<script setup lang="ts">
const { t } = useI18n()

const projects = computed(() => [
  {
    title: t('home.projects.items.ids_starter.title'),
    description: t('home.projects.items.ids_starter.description'),
    period: 'Jun 2022 - Present',
    company: 'PT. Inovasi Dinamika Solusi',
    icon: 'i-lucide-box',
    features: [
      'MySQL',
      'Laravel',
      'PHP',
      'HTML5',
      'Docker',
      'JavaScript',
      'PostgreSQL',
      'Vue.js',
      'CSS'
    ]
  },
  {
    title: t('home.projects.items.sakti.title'),
    description: t('home.projects.items.sakti.description'),
    period: 'May 2024 - Jul 2025',
    company: 'PT. Inovasi Dinamika Solusi',
    icon: 'i-lucide-fingerprint',
    image: '/images/projects/sakti.png',
    features: [
      'Laravel',
      'Vue.js',
      'DeepFace',
      'PostgreSQL',
      'Redis',
      'Odoo',
      'Soketi'
    ]
  },
  {
    title: t('home.projects.items.folur.title'),
    description: t('home.projects.items.folur.description'),
    period: 'Jul 2024 - Oct 2024',
    company: 'PT. Inovasi Dinamika Solusi',
    icon: 'i-lucide-globe',
    image: '/images/projects/folur-web.png',
    features: [
      'Python',
      'JavaScript',
      'Leaflet',
      'Odoo',
      'PostgreSQL',
      'Nginx'
    ]
  },
  {
    title: t('home.projects.items.tekmira.title'),
    description: t('home.projects.items.tekmira.description'),
    period: 'Dec 2023 - Mar 2024',
    company: 'PT. Inovasi Dinamika Solusi',
    icon: 'i-lucide-flask-conical',
    image: '/images/projects/tekmira-uprof.png',
    features: [
      'Laravel',
      'Vue.js',
      'MySQL',
      'Redis',
      'REST APIs',
      'ISO 17025'
    ]
  },
  {
    title: t('home.projects.items.malaria.title'),
    description: t('home.projects.items.malaria.description'),
    period: 'Apr 2023 - Sep 2023',
    company: 'PT. Inovasi Dinamika Solusi',
    icon: 'i-simple-icons-drupal',
    image: '/images/projects/malaria-web.png',
    features: [
      'Drupal 9.5',
      'Health Governance',
      'UNDP Partnership',
      'Grant Management'
    ]
  },
  {
    title: t('home.projects.items.slide_babel.title'),
    description: t('home.projects.items.slide_babel.description'),
    period: 'Jul 2023 - Sep 2023',
    company: 'PT. Inovasi Dinamika Solusi',
    icon: 'i-lucide-fish',
    image: '/images/projects/slide-babel.png',
    features: [
      'Fisheries Data',
      'Price Monitoring',
      'Stock Availability',
      'Location Mapping'
    ]
  },
  {
    title: t('home.projects.items.rabbani.title'),
    description: t('home.projects.items.rabbani.description'),
    period: 'Nov 2022 - Jun 2023',
    company: 'PT. Inovasi Dinamika Solusi',
    icon: 'i-lucide-shopping-bag',
    image: '/images/projects/rabbani.png',
    features: [
      'Vue.js',
      'Node.js',
      'CSS',
      'E-commerce'
    ]
  },
  {
    title: t('home.projects.items.clove.title'),
    description: t('home.projects.items.clove.description'),
    period: 'Jan 2023 - May 2023',
    company: 'PT. Inovasi Dinamika Solusi',
    icon: 'i-lucide-bar-chart-3',
    image: '/images/projects/clove-analytics.png',
    features: [
      'Laravel',
      'Vue.js',
      'R Language',
      'PostgreSQL',
      'Statistical Analysis'
    ]
  },
  {
    title: t('home.projects.items.koni_atlet.title'),
    description: t('home.projects.items.koni_atlet.description'),
    period: 'Jun 2022 - May 2023',
    company: 'PT. Inovasi Dinamika Solusi',
    icon: 'i-lucide-medal',
    image: '/images/projects/koni-jabar-atlet.png',
    features: [
      'MySQL',
      'PHP',
      'CodeIgniter',
      'UI Kit',
      'Athlete Tracking'
    ]
  },
  {
    title: t('home.projects.items.starsender.title'),
    description: t('home.projects.items.starsender.description'),
    period: 'Apr 2023 - Apr 2023',
    company: 'Freelance',
    icon: 'i-simple-icons-whatsapp',
    image: '/images/projects/starsender.png',
    features: [
      'PHP',
      'REST APIs',
      'WhatsApp API',
      'WHMCS Integration'
    ]
  },
  {
    title: t('home.projects.items.favori.title'),
    description: t('home.projects.items.favori.description'),
    period: 'Oct 2022 - Mar 2023',
    company: 'Inacookies',
    icon: 'i-lucide-layout',
    image: '/images/projects/favori-app.png',
    features: [
      'Laravel',
      'Vue.js',
      'MySQL',
      'REST APIs',
      'Dashboard'
    ]
  },
  {
    title: t('home.projects.items.mtre3.title'),
    description: t('home.projects.items.mtre3.description'),
    period: 'Jun 2022 - Mar 2023',
    company: 'PT. Inovasi Dinamika Solusi',
    icon: 'i-lucide-sun',
    features: [
      'PHP',
      'MySQL',
      'UIKit',
      'Grant System',
      'UNDP Project'
    ]
  },
  {
    title: t('home.projects.items.koni_dashboard.title'),
    description: t('home.projects.items.koni_dashboard.description'),
    period: 'Jul 2022 - Nov 2022',
    company: 'PT. Inovasi Dinamika Solusi',
    icon: 'i-lucide-layout-dashboard',
    image: '/images/projects/koni-jabar-dashboard.png',
    features: [
      'CodeIgniter',
      'MySQL',
      'Data Visualization',
      'Sports Analytics'
    ]
  },
  {
    title: t('home.projects.items.koni_website.title'),
    description: t('home.projects.items.koni_website.description'),
    period: 'Jul 2022 - Nov 2022',
    company: 'PT. Inovasi Dinamika Solusi',
    icon: 'i-lucide-monitor',
    image: '/images/projects/konijabar-website.png',
    features: [
      'CodeIgniter',
      'PHP',
      'MySQL',
      'Web Maintenance'
    ]
  },
  {
    title: t('home.projects.items.frozen_food.title'),
    description: t('home.projects.items.frozen_food.description'),
    period: 'Nov 2021 - Aug 2022',
    company: 'Ritel Makanan Beku',
    icon: 'i-lucide-snowflake',
    features: [
      'Laravel',
      'Bootstrap',
      'MySQL',
      'E-commerce',
      'Inventory'
    ]
  },
  {
    title: t('home.projects.items.undss.title'),
    description: t('home.projects.items.undss.description'),
    period: 'Jun 2022 - Jul 2022',
    company: 'PT. Inovasi Dinamika Solusi',
    icon: 'i-lucide-shield-alert',
    image: '/images/projects/undss-dashboard.png',
    features: [
      'CodeIgniter',
      'PHP',
      'MySQL',
      'Spatial Analysis',
      'Risk Management'
    ]
  },
  {
    title: t('home.projects.items.zafaa.title'),
    description: t('home.projects.items.zafaa.description'),
    period: 'Apr 2022 - Jun 2022',
    company: 'Ritel Makanan Beku',
    icon: 'i-lucide-shopping-cart',
    features: [
      'Laravel',
      'PHP',
      'JavaScript',
      'POS System'
    ]
  }
])

useSeoMeta({
  title: 'Projects - Muhammad Rheza Alfin',
  description: 'A collection of my projects and technical achievements.'
})

const links = computed(() => [
  {
    label: t('projectsPage.getInTouch'),
    icon: 'i-lucide-mail',
    color: 'primary',
    to: 'mailto:m.rheza.alfin@gmail.com',
    size: 'xl'
  }
])
</script>

<template>
  <div>
    <UPageHero :title="t('projectsPage.title')" :description="t('projectsPage.description')" align="center"
      :links="links">
      <template #top>
        <HeroBackground />
      </template>
    </UPageHero>

    <UContainer class="mt-24">
      <div class="flex flex-col gap-16 md:gap-24 pb-24">
        <div v-for="(project, index) in projects" :key="index" class="grid lg:grid-cols-2 gap-8 lg:gap-16 items-start">
          <!-- Image Side -->
          <div :class="[index % 2 === 1 ? 'lg:order-1' : 'lg:order-2']">
            <div
              class="relative aspect-video w-full rounded-xl overflow-hidden border border-gray-200 dark:border-gray-800 bg-gray-100 dark:bg-gray-900 flex items-center justify-center group">
              <img :src="project.image || '/images/projects/default.png'" :alt="project.title"
                class="w-full h-full object-cover object-top transition-transform duration-500 group-hover:scale-105">
            </div>
          </div>

          <!-- Content Side -->
          <div :class="[index % 2 === 1 ? 'lg:order-2' : 'lg:order-1']">
            <div class="flex items-center gap-3 mb-4">
              <UIcon :name="project.icon" class="w-8 h-8 text-primary" />
              <h2 class="text-3xl font-bold text-gray-900 dark:text-white">
                {{ project.title }}
              </h2>
            </div>

            <div class="space-y-4">
              <p class="text-lg text-gray-600 dark:text-gray-300">
                {{ project.description }}
              </p>

              <div class="flex flex-wrap gap-4 text-sm font-medium text-gray-500 dark:text-gray-400 mb-6">
                <div class="flex items-center gap-1.5">
                  <UIcon name="i-lucide-calendar" class="w-4 h-4" />
                  <span>{{ project.period }}</span>
                </div>
                <div class="flex items-center gap-1.5">
                  <UIcon name="i-lucide-building-2" class="w-4 h-4" />
                  <span>{{ project.company }}</span>
                </div>
              </div>

              <div class="grid grid-cols-1 sm:grid-cols-2 gap-y-3 gap-x-6">
                <div v-for="feature in project.features" :key="feature"
                  class="flex items-center gap-2 text-gray-600 dark:text-gray-300">
                  <UIcon name="i-lucide-check-circle" class="w-5 h-5 text-primary flex-shrink-0" />
                  <span>{{ feature }}</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <AppCTA />
    </UContainer>
  </div>
</template>
