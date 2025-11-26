<script setup lang="ts">
const cta = {
  title: 'Let\'s Build Something <span class="text-primary">Together</span>',
  description: 'Let\'s collaborate to build something exceptional. I\'m ready to partner with you to transform your ideas into impactful solutions. Together, we can create technology that drives real progress.',
  links: [
    {
      label: 'Get in Touch',
      to: 'mailto:m.rheza.alfin@gmail.com',
      trailingIcon: 'i-lucide-mail'
    },
    {
      label: 'View GitHub',
      to: 'https://github.com/vheins',
      target: '_blank',
      variant: 'subtle',
      icon: 'i-simple-icons-github'
    }
  ]
}
</script>

<template>
  <div class="relative">
    <USeparator />
    <UPageCTA
      v-bind="cta"
      variant="naked"
      class="overflow-hidden @container"
    >
      <template #title>
        <span
          class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl"
          v-html="cta.title"
        />

        <div class="@max-[1280px]:hidden">
          <UColorModeImage
            light="/images/light/line-6.svg"
            dark="/images/dark/line-6.svg"
            class="absolute left-10 -top-10 sm:top-0 h-full"
          />
          <UColorModeImage
            light="/images/light/line-7.svg"
            dark="/images/dark/line-7.svg"
            class="absolute right-0 bottom-0 h-full"
          />
        </div>
      </template>

      <LazyStarsBg />
    </UPageCTA>
  </div>
</template>
