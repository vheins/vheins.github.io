<script setup lang="ts">
const { t } = useI18n()

const services = computed(() => [
  {
    title: t('servicesPage.items.finance.title'),
    description: t('servicesPage.items.finance.description'),
    modules: ['Sales', 'Purchase', 'Accounting'],
    icon: 'i-lucide-banknote'
  },
  {
    title: t('servicesPage.items.supplyChain.title'),
    description: t('servicesPage.items.supplyChain.description'),
    modules: ['Sales', 'Purchase', 'Accounting', 'Inventory'],
    icon: 'i-lucide-truck'
  },
  {
    title: t('servicesPage.items.manufacturing.title'),
    description: t('servicesPage.items.manufacturing.description'),
    modules: ['Sales', 'Purchase', 'Accounting', 'Inventory', 'Manufacturing'],
    icon: 'i-lucide-factory'
  },
  {
    title: t('servicesPage.items.ecommerce.title'),
    description: t('servicesPage.items.ecommerce.description'),
    modules: ['Sales', 'Purchase', 'Accounting', 'Inventory', 'Website Builder', 'Integrasi Payment & Shipping Gateway'],
    icon: 'i-lucide-shopping-bag'
  },
  {
    title: t('servicesPage.items.hr.title'),
    description: t('servicesPage.items.hr.description'),
    modules: ['Employees', 'Attendance', 'Time Off', 'Payroll'],
    icon: 'i-lucide-users'
  },
  {
    title: t('servicesPage.items.website.title'),
    description: t('servicesPage.items.website.description'),
    modules: ['Website Company Profile'],
    icon: 'i-lucide-globe'
  },
  {
    title: t('servicesPage.items.elearning.title'),
    description: t('servicesPage.items.elearning.description'),
    modules: ['Website Builder', 'E-Learning', 'Tests'],
    icon: 'i-lucide-graduation-cap'
  },
  {
    title: t('servicesPage.items.project.title'),
    description: t('servicesPage.items.project.description'),
    modules: ['Project', 'Timesheet', 'Sales', 'Purchase', 'Accounting'],
    icon: 'i-lucide-kanban'
  },
  {
    title: t('servicesPage.items.custom.title'),
    description: t('servicesPage.items.custom.description'),
    modules: ['Python', 'XML', 'PostgreSQL', 'API Integration'],
    icon: 'i-lucide-code-2'
  },
  {
    title: t('servicesPage.items.training.title'),
    description: t('servicesPage.items.training.description'),
    modules: ['Functional Training', 'Technical Training', 'Documentation'],
    icon: 'i-lucide-presentation'
  }
])

useSeoMeta({
  title: 'Services - Muhammad Rheza Alfin',
  description: 'ERP Implementation and IT Services'
})

const links = computed(() => [
  {
    label: t('servicesPage.getInTouch'),
    icon: 'i-lucide-mail',
    color: 'primary',
    to: 'mailto:m.rheza.alfin@gmail.com',
    size: 'xl'
  }
])
</script>

<template>
  <div>
    <UPageHero :title="t('servicesPage.title')" :description="t('servicesPage.description')" align="center"
      :links="links">
      <template #top>
        <HeroBackground />
      </template>
    </UPageHero>

    <UContainer class="mt-24">
      <UPageGrid class="pb-24">
        <UPageCard v-for="(service, index) in services" :key="index" :title="service.title"
          :description="service.description" :icon="service.icon">
          <template #footer>
            <div class="flex flex-wrap gap-2">
              <UBadge v-for="modul in service.modules" :key="modul" color="neutral" variant="subtle" size="sm">
                {{ modul }}
              </UBadge>
            </div>
          </template>
        </UPageCard>
      </UPageGrid>
      <AppCTA />
    </UContainer>
  </div>
</template>
