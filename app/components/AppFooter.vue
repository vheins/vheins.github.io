<script setup lang="ts">
const columns = [{
  label: 'Navigation',
  children: [{
    label: 'About',
    to: '/#steps'
  }, {
    label: 'Skills',
    to: '/#features'
  }, {
    label: 'Projects',
    to: '/projects'
  }, {
    label: 'Contact',
    to: 'mailto:m.rheza.alfin@gmail.com'
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
}]
</script>

<template>
  <USeparator
    icon="i-simple-icons-nuxtdotjs"
    class="h-px"
  />

  <UFooter :ui="{ top: 'border-b border-default' }">
    <template #top>
      <UContainer>
        <UFooterColumns :columns="columns" />
      </UContainer>
    </template>

    <template #left>
      <p class="text-sm text-muted">
        Built with Nuxt UI • © {{ new Date().getFullYear() }} Muhammad Rheza Alfin
      </p>
    </template>

    <template #right>
      <UButton
        to="https://github.com/vheins"
        target="_blank"
        icon="i-simple-icons-github"
        aria-label="GitHub Profile"
        color="neutral"
        variant="ghost"
      />
      <UButton
        to="https://www.linkedin.com/in/arhez"
        target="_blank"
        icon="i-simple-icons-linkedin"
        aria-label="LinkedIn Profile"
        color="neutral"
        variant="ghost"
      />
      <UButton
        to="mailto:m.rheza.alfin@gmail.com"
        icon="i-lucide-mail"
        aria-label="Email"
        color="neutral"
        variant="ghost"
      />
    </template>
  </UFooter>
</template>
