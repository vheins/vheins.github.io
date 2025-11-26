<script setup lang="ts">
const nuxtApp = useNuxtApp()
const route = useRoute()
const { activeHeadings, updateHeadings } = useScrollspy()

const { t } = useI18n()

const items = computed(() => [{
  label: t('nav.about'),
  to: '/#steps',
  active: activeHeadings.value.includes('steps') && route.path === '/'
}, {
  label: t('nav.skills'),
  to: '/#features',
  active: activeHeadings.value.includes('features') && route.path === '/'
}, {
  label: t('nav.journey'),
  to: '/journey',
  active: route.path === '/journey'
}, {
  label: t('nav.services'),
  to: '/services',
  active: route.path === '/services'
}, {
  label: t('nav.projects'),
  to: '/projects',
  active: route.path === '/projects'
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
        Muhammad Rheza Alfin
      </NuxtLink>
    </template>

    <template #right>
      <UNavigationMenu :items="items" variant="link" class="hidden lg:block" />

      <UButton label="Contact" variant="subtle" to="mailto:m.rheza.alfin@gmail.com" class="hidden lg:block" />

      <AppLocaleSelect class="w-48" />

      <UColorModeButton />
    </template>

    <template #body>
      <UNavigationMenu :items="items" orientation="vertical" class="-mx-2.5" />
      <UButton class="mt-4" label="Contact" variant="subtle" to="mailto:m.rheza.alfin@gmail.com" block />
      <AppLocaleSelect class="mt-2" />
    </template>
  </UHeader>
</template>
