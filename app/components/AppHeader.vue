<script setup lang="ts">
const nuxtApp = useNuxtApp()
const route = useRoute()
const { activeHeadings, updateHeadings } = useScrollspy()

const { t } = useI18n()

const localePath = useLocalePath()

const items = computed(() => [{
  label: t('nav.about'),
  to: localePath('/#steps'),
  active: activeHeadings.value.includes('steps') && route.path === localePath('/')
}, {
  label: t('nav.skills'),
  to: localePath('/#features'),
  active: activeHeadings.value.includes('features') && route.path === localePath('/')
}, {
  label: t('nav.journey'),
  to: localePath('/journey'),
  active: route.path === localePath('/journey')
}, {
  label: t('nav.services'),
  to: localePath('/services'),
  active: route.path === localePath('/services')
}, {
  label: t('nav.projects'),
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
      <NuxtLink :to="localePath('/')">
        Muhammad Rheza Alfin
      </NuxtLink>
    </template>

    <template #right>
      <UNavigationMenu :items="items" variant="link" class="hidden lg:block" />

      <UButton :label="t('nav.contact')" variant="subtle" to="mailto:m.rheza.alfin@gmail.com" class="hidden lg:block" />

      <AppLocaleSelect class="w-48" />

      <UColorModeButton />
    </template>

    <template #body>
      <UNavigationMenu :items="items" orientation="vertical" class="-mx-2.5" />
      <UButton class="mt-4" :label="t('nav.contact')" variant="subtle" to="mailto:m.rheza.alfin@gmail.com" block />
      <AppLocaleSelect class="mt-2" />
    </template>
  </UHeader>
</template>
