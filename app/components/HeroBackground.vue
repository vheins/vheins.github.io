<script setup lang="ts">
const canvasRef = ref<HTMLCanvasElement | null>(null)
const colorMode = useColorMode()

// Configuration
const particleCount = 40
const connectionDistance = 200
const moveSpeed = 1

interface Particle {
  x: number
  y: number
  vx: number
  vy: number
  size: number
}

interface Packet {
  from: number
  to: number
  progress: number
  speed: number
}

const particles = ref<Particle[]>([])
const packets = ref<Packet[]>([])
let animationId: number

const initParticles = (width: number, height: number) => {
  particles.value = []
  for (let i = 0; i < particleCount; i++) {
    particles.value.push({
      x: Math.random() * width,
      y: Math.random() * height,
      vx: (Math.random() - 0.5) * moveSpeed,
      vy: (Math.random() - 0.5) * moveSpeed,
      size: Math.random() * 4 + 2 // Square size
    })
  }
}

const draw = () => {
  const canvas = canvasRef.value
  if (!canvas) return
  const ctx = canvas.getContext('2d')
  if (!ctx) return

  const w = canvas.width
  const h = canvas.height

  ctx.clearRect(0, 0, w, h)

  const isDark = colorMode.value === 'dark'
  // Colors
  const particleColor = isDark ? 'rgba(255, 255, 255, 0.3)' : 'rgba(0, 0, 0, 0.3)'
  const lineColor = isDark ? 'rgba(255, 255, 255, 0.05)' : 'rgba(0, 0, 0, 0.05)'
  // Use the primary color for packets (approximate hex for standard primary, or could use computed style)
  const packetColor = isDark ? '#10B981' : '#059669'

  // Update and draw particles
  particles.value.forEach((p, i) => {
    p.x += p.vx
    p.y += p.vy

    if (p.x < 0 || p.x > w) p.vx *= -1
    if (p.y < 0 || p.y > h) p.vy *= -1

    ctx.fillStyle = particleColor
    ctx.beginPath()
    // Draw square for "block" look
    ctx.rect(p.x - p.size / 2, p.y - p.size / 2, p.size, p.size)
    ctx.fill()

    // Connections
    for (let j = i + 1; j < particles.value.length; j++) {
      const p2 = particles.value[j]
      const dx = p.x - p2.x
      const dy = p.y - p2.y
      const dist = Math.sqrt(dx * dx + dy * dy)

      if (dist < connectionDistance) {
        ctx.strokeStyle = lineColor
        ctx.lineWidth = 1
        ctx.beginPath()
        ctx.moveTo(p.x, p.y)
        ctx.lineTo(p2.x, p2.y)
        ctx.stroke()

        // Spawn packet
        if (Math.random() < 0.005) {
          packets.value.push({
            from: i,
            to: j,
            progress: 0,
            speed: 0.01 + Math.random() * 0.02
          })
        }
      }
    }
  })

  // Update and draw packets
  for (let i = packets.value.length - 1; i >= 0; i--) {
    const pkt = packets.value[i]
    if (!pkt) continue

    pkt.progress += pkt.speed

    if (pkt.progress >= 1) {
      packets.value.splice(i, 1)
      continue
    }

    const p1 = particles.value[pkt.from]
    const p2 = particles.value[pkt.to]

    if (!p1 || !p2) continue

    const x = p1.x + (p2.x - p1.x) * pkt.progress
    const y = p1.y + (p2.y - p1.y) * pkt.progress

    ctx.fillStyle = packetColor
    ctx.beginPath()
    ctx.rect(x - 1.5, y - 1.5, 3, 3)
    ctx.fill()
  }

  animationId = requestAnimationFrame(draw)
}

const resizeCanvas = () => {
  if (canvasRef.value) {
    const parent = canvasRef.value.parentElement
    if (parent) {
      canvasRef.value.width = parent.clientWidth
      canvasRef.value.height = parent.clientHeight
      if (particles.value.length === 0) {
        initParticles(parent.clientWidth, parent.clientHeight)
      }
    }
  }
}

onMounted(() => {
  resizeCanvas()
  draw()
  window.addEventListener('resize', resizeCanvas)
})

onUnmounted(() => {
  cancelAnimationFrame(animationId)
  window.removeEventListener('resize', resizeCanvas)
})
</script>

<template>
  <div class="absolute inset-0 overflow-hidden pointer-events-none -z-10 w-full h-full">
    <canvas
      ref="canvasRef"
      class="w-full h-full opacity-100"
    />
    <!-- Gradient overlay for text readability -->
    <div
      class="absolute inset-0 bg-gradient-to-b from-transparent via-white/80 to-white dark:via-gray-900/80 dark:to-gray-900"
    />
  </div>
</template>
```
