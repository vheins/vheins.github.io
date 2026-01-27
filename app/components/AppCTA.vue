<script setup lang="ts">
// Hardcoded corporate CTA to ensure consistency
const cta = computed(() => ({
  title: 'Partner With Us',
  description: 'Ready to transform your business? Let\'s discuss how our technology solutions can drive your success.',
  links: [
    {
      label: 'Contact Us',
      to: 'mailto:inquiry@vheins.com',
      trailingIcon: 'i-lucide-mail'
    },
    {
      label: 'Schedule Consultation',
      to: '#',
      target: '_blank',
      variant: 'subtle',
      icon: 'i-lucide-calendar'
    }
  ]
}))
</script>

<template>
  <div class="relative">
    <USeparator />
    <UPageCTA v-bind="cta" variant="naked" class="overflow-hidden @container">
      <template #title>
        <span class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl">
          Partner With <span class="text-primary">Us</span>
        </span>

        <div class="@max-[1280px]:hidden">
          <UColorModeImage light="/images/light/line-6.svg" dark="/images/dark/line-6.svg"
            class="absolute left-10 -top-10 sm:top-0 h-full" />
          <UColorModeImage light="/images/light/line-7.svg" dark="/images/dark/line-7.svg"
            class="absolute right-0 bottom-0 h-full" />
        </div>
      </template>

      <LazyStarsBg />
    </UPageCTA>
  </div>
</template>
