<script setup lang="ts">
const nuxtApp = useNuxtApp()
const route = useRoute()
const { activeHeadings, updateHeadings } = useScrollspy()

const localePath = useLocalePath()

// Hardcoded corporate navigation to replace i18n personal links
const items = computed(() => [{
  label: 'About',
  to: localePath('/#steps'),
  active: activeHeadings.value.includes('steps') && route.path === localePath('/')
}, {
  label: 'Capabilities',
  to: localePath('/#features'),
  active: activeHeadings.value.includes('features') && route.path === localePath('/')
}, {
  label: 'Company',
  to: localePath('/journey'),
  active: route.path === localePath('/journey')
}, {
  label: 'Services',
  to: localePath('/services'),
  active: route.path === localePath('/services')
}, {
  label: 'Success Stories',
  to: localePath('/projects'),
  active: route.path === localePath('/projects')
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
      <NuxtLink :to="localePath('/')" class="font-bold text-xl text-primary">
        Vheins Technologies
      </NuxtLink>
    </template>

    <template #right>
      <UNavigationMenu :items="items" variant="link" class="hidden lg:block" />

      <UButton label="Contact Us" variant="subtle" to="mailto:inquiry@vheins.com" class="hidden lg:block" />

      <AppLocaleSelect class="hidden lg:block w-48" />

      <UColorModeButton />
    </template>

    <template #body>
      <UNavigationMenu :items="items" orientation="vertical" class="-mx-2.5" />
      <UButton class="mt-4" label="Contact Us" variant="subtle" to="mailto:inquiry@vheins.com" block />
      <AppLocaleSelect class="mt-2" />
    </template>
  </UHeader>
</template>
