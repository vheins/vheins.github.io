<script setup lang="ts">
import { en, id } from '@nuxt/ui/locale'
const { locale, setLocale } = useI18n()
</script>

<template>
  <ULocaleSelect :model-value="locale" :locales="[en, id]" @update:model-value="setLocale($event as any)" />
</template>
