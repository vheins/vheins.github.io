<script setup lang="ts">
const columns = [{
  label: 'Navigation',
  children: [{
    label: 'About'
  }, {
    label: 'Skills'
  }, {
    label: 'Projects'
  }, {
    label: 'Contact'
  }]
}, {
  label: 'Technologies',
  children: [{
    label: 'Laravel'
  }, {
    label: 'Vue.js'
  }, {
    label: 'PostgreSQL'
  }, {
    label: 'Docker'
  }]
}, {
  label: 'Connect',
  children: [{
    label: 'GitHub'
  }, {
    label: 'LinkedIn'
  }, {
    label: 'Email'
  }]
}]

const toast = useToast()

const email = ref('')
const loading = ref(false)

function onSubmit() {
  loading.value = true

  toast.add({
    title: 'Subscribed!',
    description: 'You\'ve been subscribed to our newsletter.'
  })
}
</script>

<template>
  <USeparator icon="i-simple-icons-nuxtdotjs" class="h-px" />

  <UFooter :ui="{ top: 'border-b border-default' }">
    <template #top>
      <UContainer>
        <UFooterColumns :columns="columns">
          <template #right>
            <form @submit.prevent="onSubmit">
              <UFormField name="email" label="Subscribe to our newsletter" size="lg">
                <UInput v-model="email" type="email" class="w-full" placeholder="Enter your email">
                  <template #trailing>
                    <UButton type="submit" size="xs" label="Subscribe" />
                  </template>
                </UInput>
              </UFormField>
            </form>
          </template>
        </UFooterColumns>
      </UContainer>
    </template>

    <template #left>
      <p class="text-sm text-muted">
        Built with Nuxt UI • © {{ new Date().getFullYear() }} Vheins
      </p>
    </template>

    <template #right>
      <UButton to="https://github.com/vheins" target="_blank" icon="i-simple-icons-github" aria-label="GitHub Profile"
        color="neutral" variant="ghost" />
      <UButton to="https://linkedin.com/in/vheins" target="_blank" icon="i-simple-icons-linkedin"
        aria-label="LinkedIn Profile" color="neutral" variant="ghost" />
      <UButton to="mailto:your.email@example.com" icon="i-lucide-mail" aria-label="Email" color="neutral"
        variant="ghost" />
    </template>
  </UFooter>
</template>
