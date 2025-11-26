<script setup lang="ts">
const projects = [
  {
    title: 'IDS Starter Kit',
    description: 'The FullStack Application Starter Kit utilizes the Laravel framework, VueJS, UI Kit, and is Docker-friendly. This comprehensive starter kit provides developers with a solid foundation to kickstart full-stack application development. Laravel offers a robust backend structure, while VueJS powers the frontend with dynamic user interfaces. The UI Kit enhances visual appeal, and Docker ensures seamless deployment and scalability.',
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
    title: 'Sistem Absensi dan Laporan Terintegrasi (Sakti)',
    description: 'Integrated attendance and reporting system for PT Pesonna Optima Jasa. Features DeepFace facial recognition for accurate clock-in/out procedures and comprehensive reporting tools to streamline employee management.',
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
    title: 'Folur Global Platform',
    description: 'The Food Systems, Land Use, and Restoration (FOLUR) initiative transforms agricultural practices and land use across 27 countries to support sustainability, food security, and restoration. Supported by the GEF, it employs a landscape-based approach to strengthen sustainable value chains. In Indonesia, the program emphasizes sustainable agriculture, ecosystem health, and smallholder farmer capacity building.',
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
    title: 'tekMIRA - Uji Profisiensi',
    description: 'Proficiency testing platform for the Mineral and Coal Testing Center (BBPMB tekMIRA). Facilitates ISO 17025 compliance for laboratories testing coal and minerals, ensuring reliable analytical results and performance evaluation.',
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
    title: 'Malaria Website with Drupal 9.5',
    description: 'Developed for the UNDP HEART Program to support health inequality efforts. Strengthens the Global Fund\'s Country Coordinating Mechanisms (CCM) in Indonesia, improving grant management and government-civil society coordination.',
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
    title: 'Slide Babel - Sistem Informasi Perikanan',
    description: 'Fisheries information platform for Bangka Belitung Province. Provides real-time data on fish prices, stocks, cultivated types, and market locations, connecting the community with up-to-date fisheries information.',
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
    title: 'Rabbani Web Commerce',
    description: 'E-commerce platform for Islamic-based products, focusing on ethical production and sustainability. Features a secure, user-friendly interface aligned with Islamic values to enhance the shopping experience.',
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
    title: 'Clove Analytics Dashboard',
    description: 'Statistical analysis tool for Clove Research. Includes modules for significant tests, brand mapping, and propensity score matching, along with user subscription management and interactive dashboards.',
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
    title: 'Koni Jabar Atlet Management',
    description: 'Comprehensive platform for managing West Java athlete data, training programs, and achievements. Serves as a centralized information hub for tracking sports development and coaching effectiveness.',
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
    title: 'Starsender Plugin for WHMCS',
    description: 'WhatsApp API integration plugin for WHMCS. Enables businesses to send automated messages and notifications directly from the dashboard, enhancing client communication and engagement.',
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
    title: 'Favori App V2',
    description: 'Internal operational dashboard for Inacookies. Centralizes monitoring of sales, production, inventory, and customer feedback, providing real-time insights to drive efficiency and business growth.',
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
    title: 'MTRE3 Insentif Surya Atap',
    description: 'Grant application platform for the Roof Solar Power Incentive (PLTS Atap) under the UNDP MTRE3 project. Facilitates the distribution of SEF grants to support renewable energy adoption in Indonesia.',
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
    title: 'Koni Jabar Dashboard',
    description: 'Interactive dashboard for the West Java Sports Resource Data Center. Visualizes athlete statistics, training progress, and achievements to support data-driven decision-making in sports management.',
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
    title: 'Koni Jabar Website',
    description: 'Maintenance and feature enhancement for the Koni Jabar website. Focused on performance optimization, bug fixing, and improving user experience to ensure smooth operation.',
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
    title: 'Frozen Food Dashboard & E-Commerce',
    description: 'Integrated e-commerce and warehouse management system for frozen food retail. Streamlines inventory control, purchasing, and online transactions to improve operational efficiency.',
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
    title: 'UNDSS Dashboard',
    description: 'Incident management dashboard for UNDSS. Processes and visualizes security incident data with spatial analysis tools to support risk assessment and resource allocation.',
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
    title: 'Zafaa POS',
    description: 'Specialized Point of Sale (POS) application for frozen food retail. Features stock monitoring, payment integration, and customer management to streamline daily sales operations.',
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
]

useSeoMeta({
  title: 'Projects - Muhammad Rheza Alfin',
  description: 'A collection of my projects and technical achievements.'
})
</script>

<template>
  <UContainer>
    <UPageHero
      title="Featured Projects"
      description="A comprehensive list of projects I have delivered, ranging from enterprise resource planning to specialized dashboards and e-commerce platforms."
      align="center"
    />

    <div class="flex flex-col gap-16 md:gap-24 pb-24">
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="grid lg:grid-cols-2 gap-8 lg:gap-16 items-start"
      >
        <!-- Content Side -->
        <div :class="[index % 2 === 1 ? 'lg:order-2' : '']">
          <div class="flex items-center gap-3 mb-4">
            <UIcon
              :name="project.icon"
              class="w-8 h-8 text-primary"
            />
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
                <UIcon
                  name="i-lucide-calendar"
                  class="w-4 h-4"
                />
                <span>{{ project.period }}</span>
              </div>
              <div class="flex items-center gap-1.5">
                <UIcon
                  name="i-lucide-building-2"
                  class="w-4 h-4"
                />
                <span>{{ project.company }}</span>
              </div>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 gap-y-3 gap-x-6">
              <div
                v-for="feature in project.features"
                :key="feature"
                class="flex items-center gap-2 text-gray-600 dark:text-gray-300"
              >
                <UIcon
                  name="i-lucide-check-circle"
                  class="w-5 h-5 text-primary flex-shrink-0"
                />
                <span>{{ feature }}</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Image Side -->
        <div :class="[index % 2 === 1 ? 'lg:order-1' : '']">
          <div
            class="relative aspect-video w-full rounded-xl overflow-hidden border border-gray-200 dark:border-gray-800 bg-gray-100 dark:bg-gray-900 flex items-center justify-center group"
          >
            <img
              :src="project.image || '/images/projects/default.png'"
              :alt="project.title"
              class="w-full h-full object-cover object-top transition-transform duration-500 group-hover:scale-105"
            >
          </div>
        </div>
      </div>
    </div>
  </UContainer>
</template>
