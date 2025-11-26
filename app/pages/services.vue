<script setup lang="ts">
const services = [
  {
    title: 'Finance',
    description: 'Streamline financial operations with integrated invoicing, bill payments, and comprehensive accounting reports. Automate reconciliation and ensure financial compliance.',
    modules: ['Sales', 'Purchase', 'Accounting'],
    icon: 'i-lucide-banknote'
  },
  {
    title: 'Supply Chain',
    description: 'Optimize inventory flows with integrated procurement and sales. Manage stock levels, automate replenishment, and track product movements across warehouses.',
    modules: ['Sales', 'Purchase', 'Accounting', 'Inventory'],
    icon: 'i-lucide-truck'
  },
  {
    title: 'Manufacturing',
    description: 'Manage complete production lifecycles with Bill of Materials (BOMs) and Work Orders. Integrate manufacturing with inventory and procurement for just-in-time efficiency.',
    modules: ['Sales', 'Purchase', 'Accounting', 'Inventory', 'Manufacturing'],
    icon: 'i-lucide-factory'
  },
  {
    title: 'Supply Chain & Ecommerce',
    description: 'Unify online and offline sales with a fully integrated e-commerce platform. Sync inventory in real-time, manage shipping, and accept online payments seamlessly.',
    modules: ['Sales', 'Purchase', 'Accounting', 'Inventory', 'Website Builder', 'Integrasi Payment & Shipping Gateway'],
    icon: 'i-lucide-shopping-bag'
  },
  {
    title: 'Human Resources',
    description: 'Centralize employee management from recruitment to payroll. Track attendance, manage leave requests, and automate payroll processing with local regulation compliance.',
    modules: ['Employees', 'Attendance', 'Time Off', 'Payroll'],
    icon: 'i-lucide-users'
  },
  {
    title: 'Website Company',
    description: 'Build a professional, responsive corporate website with an easy-to-use drag-and-drop builder. Showcase services and manage content without coding.',
    modules: ['Website Company Profile'],
    icon: 'i-lucide-globe'
  },
  {
    title: 'E-Learning',
    description: 'Create engaging online courses and certifications. Manage student progress, quizzes, and content delivery through a dedicated Learning Management System (LMS).',
    modules: ['Website Builder', 'E-Learning', 'Tests'],
    icon: 'i-lucide-graduation-cap'
  },
  {
    title: 'Project Management',
    description: 'Plan and track projects with tasks, timesheets, and milestones. Integrate with sales and billing to manage project profitability and resource allocation.',
    modules: ['Project', 'Timesheet', 'Sales', 'Purchase', 'Accounting'],
    icon: 'i-lucide-kanban'
  },
  {
    title: 'Custom Modul Development',
    description: 'Tailored Odoo module development to meet specific business requirements that standard modules cannot cover. Includes API integrations and workflow automation.',
    modules: ['Python', 'XML', 'PostgreSQL', 'API Integration'],
    icon: 'i-lucide-code-2'
  },
  {
    title: 'User Training',
    description: 'Comprehensive training sessions for administrators and end-users. Includes documentation, hands-on workshops, and best practice guidelines for efficient system usage.',
    modules: ['Functional Training', 'Technical Training', 'Documentation'],
    icon: 'i-lucide-presentation'
  }
]

useSeoMeta({
  title: 'Services - Muhammad Rheza Alfin',
  description: 'ERP Implementation and IT Services'
})

const links = [
  {
    label: 'Get in Touch',
    icon: 'i-lucide-mail',
    color: 'primary',
    to: 'mailto:m.rheza.alfin@gmail.com',
    size: 'xl'
  }
]
</script>

<template>
  <div>
    <UPageHero
      title="Service Implementasi ERP"
      description="Comprehensive ERP solutions tailored to your business needs."
      align="center"
      :links="links"
    >
      <template #top>
        <HeroBackground />
      </template>
    </UPageHero>

    <UContainer class="mt-24">
      <UPageGrid class="pb-24">
        <UPageCard
          v-for="(service, index) in services"
          :key="index"
          :title="service.title"
          :description="service.description"
          :icon="service.icon"
        >
          <template #footer>
            <div class="flex flex-wrap gap-2">
              <UBadge
                v-for="modul in service.modules"
                :key="modul"
                color="neutral"
                variant="subtle"
                size="sm"
              >
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
