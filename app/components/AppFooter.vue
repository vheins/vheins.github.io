<script setup lang="ts">
const { t } = useI18n()
const localePath = useLocalePath()

const columns = computed(() => [{
  label: t('footer.navigation'),
  children: [{
    label: t('nav.about'),
    to: localePath('/#steps')
  }, {
    label: t('nav.skills'),
    to: localePath('/#features')
  }, {
    label: t('nav.projects'),
    to: localePath('/projects')
  }, {
    label: t('nav.contact'),
    to: 'mailto:m.rheza.alfin@gmail.com'
  }]
}, {
  label: t('footer.technologies'),
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
  label: t('footer.connect'),
  children: [{
    label: 'GitHub',
    to: 'https://github.com/vheins',
    target: '_blank'
  }, {
    label: 'LinkedIn',
    to: 'https://www.linkedin.com/in/arhez',
    target: '_blank'
  }, {
    label: 'Email',
    to: 'mailto:m.rheza.alfin@gmail.com'
  }]
}])
</script>

<template>
  <USeparator icon="i-simple-icons-nuxtdotjs" class="h-px" />

  <UFooter :ui="{ top: 'border-b border-default' }">
    <template #top>
      <UContainer>
        <UFooterColumns :columns="columns" />
      </UContainer>
    </template>

    <template #left>
      <p class="text-sm text-muted">
        {{ t('footer.builtWith', { year: new Date().getFullYear() }) }}
      </p>
    </template>

    <template #right>
      <UButton to="https://github.com/vheins" target="_blank" icon="i-simple-icons-github" aria-label="GitHub Profile"
        color="neutral" variant="ghost" />
      <UButton to="https://www.linkedin.com/in/arhez" target="_blank" icon="i-simple-icons-linkedin"
        aria-label="LinkedIn Profile" color="neutral" variant="ghost" />
      <UButton to="mailto:m.rheza.alfin@gmail.com" icon="i-lucide-mail" aria-label="Email" color="neutral"
        variant="ghost" />
    </template>
  </UFooter>
</template>
