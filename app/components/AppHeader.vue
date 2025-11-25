<script setup lang="ts">
const nuxtApp = useNuxtApp()
const { activeHeadings, updateHeadings } = useScrollspy()

const items = computed(() => [{
  label: 'About',
  to: '#steps',
  active: activeHeadings.value.includes('steps') && !activeHeadings.value.includes('projects')
}, {
  label: 'Skills',
  to: '#features',
  active: activeHeadings.value.includes('features') && !activeHeadings.value.includes('projects')
}, {
  label: 'Projects',
  to: '#projects',
  active: activeHeadings.value.includes('projects')
}])

nuxtApp.hooks.hookOnce('page:finish', () => {
  updateHeadings([
    document.querySelector('#steps'),
    document.querySelector('#features'),
    document.querySelector('#projects')
  ].filter(Boolean) as Element[])
})
</script>

<template>
  <UHeader>
    <template #left>
      <NuxtLink to="/">
        Vheins
      </NuxtLink>
    </template>

    <template #right>
      <UNavigationMenu :items="items" variant="link" class="hidden lg:block" />

      <UButton label="Contact" variant="subtle" to="mailto:your.email@example.com" class="hidden lg:block" />

      <UColorModeButton />
    </template>

    <template #body>
      <UNavigationMenu :items="items" orientation="vertical" class="-mx-2.5" />
      <UButton class="mt-4" label="Contact" variant="subtle" to="mailto:your.email@example.com" block />
    </template>
  </UHeader>
</template>
