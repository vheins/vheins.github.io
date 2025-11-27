<script setup lang="ts">
const { t } = useI18n()

const page = computed(() => ({
  title: '',
  description: t('home.description'),
  hero: {
    links: [
      {
        label: t('home.hero.viewProjects'),
        icon: 'i-lucide-folder-git-2',
        trailing: true,
        color: 'primary',
        to: '#projects',
        size: 'xl'
      },
      {
        label: t('home.hero.github'),
        icon: 'i-simple-icons-github',
        size: 'xl',
        color: 'neutral',
        variant: 'outline',
        to: 'https://github.com/vheins',
        target: '_blank'
      },
      {
        label: t('home.hero.getInTouch'),
        icon: 'i-lucide-mail',
        size: 'xl',
        color: 'primary',
        variant: 'solid',
        to: 'mailto:m.rheza.alfin@gmail.com'
      }
    ]
  },
  section: {
    title: '',
    description: t('home.transformation.description'),
    images: {
      mobile: '/images/journey-professional.png',
      desktop: '/images/journey-professional.png'
    },
    features: [
      {
        title: t('home.transformation.features.analytical.title'),
        description: t('home.transformation.features.analytical.description'),
        class: 'border-l border-primary pl-4'
      },
      {
        title: t('home.transformation.features.detail.title'),
        description: t('home.transformation.features.detail.description'),
        class: 'border-l border-default pt-4 pl-4'
      },
      {
        title: t('home.transformation.features.improvement.title'),
        description: t('home.transformation.features.improvement.description'),
        class: 'border-l border-default pt-4 pl-4'
      }
    ]
  },
  features: {
    title: '',
    description: t('home.expertise.description'),
    features: [
      {
        title: t('home.expertise.items.backend.title'),
        description: t('home.expertise.items.backend.description'),
        icon: 'i-lucide-server',
        ui: { leading: 'bg-accented/50 p-2 rounded-md border border-muted border-dashed' }
      },
      {
        title: t('home.expertise.items.frontend.title'),
        description: t('home.expertise.items.frontend.description'),
        icon: 'i-lucide-layout-dashboard',
        ui: { leading: 'bg-accented/50 p-2 rounded-md border border-muted border-dashed' }
      },
      {
        title: t('home.expertise.items.performance.title'),
        description: t('home.expertise.items.performance.description'),
        icon: 'i-lucide-zap',
        ui: { leading: 'bg-accented/50 p-2 rounded-md border border-muted border-dashed' }
      },
      {
        title: t('home.expertise.items.devops.title'),
        description: t('home.expertise.items.devops.description'),
        icon: 'i-lucide-cloud',
        ui: { leading: 'bg-accented/50 p-2 rounded-md border border-muted border-dashed' }
      },
      {
        title: t('home.expertise.items.integration.title'),
        description: t('home.expertise.items.integration.description'),
        icon: 'i-lucide-workflow',
        ui: { leading: 'bg-accented/50 p-2 rounded-md border border-muted border-dashed' }
      },
      {
        title: t('home.expertise.items.leadership.title'),
        description: t('home.expertise.items.leadership.description'),
        icon: 'i-lucide-users',
        ui: { leading: 'bg-accented/50 p-2 rounded-md border border-muted border-dashed' }
      }
    ]
  },
  steps: {
    title: 'My <span class="text-primary">Journey</span>',
    description: 'From inventory control to cloud infrastructure - every step has built who I am today.',
    items: [
      {
        title: 'PT. Inovasi Dinamika Solusi',
        description: 'Software Development Team Lead (Jan 2023 - Present) • Full-stack Developer (Jun 2022 - Jan 2023). Leading development teams and building full-stack solutions in Bandung, West Java.',
        image: {
          light: '/images/light/track.svg',
          dark: '/images/dark/track.svg'
        }
      },
      {
        title: 'Ritel Makanan Beku',
        description: 'Full-stack Developer (Oct 2021 - Jun 2022). Developed web applications and managed digital solutions for retail operations.',
        image: {
          light: '/images/light/optimize.svg',
          dark: '/images/dark/optimize.svg'
        }
      },
      {
        title: 'PT. Favori Corp Sedaya',
        description: 'Head Of Sales Operations (Aug 2020 - Oct 2021). Managed sales operations and optimized business processes.',
        image: {
          light: '/images/light/connect.svg',
          dark: '/images/dark/connect.svg'
        }
      },
      {
        title: 'Indomaret Group',
        description: 'Inventory Control Supervisor (Aug 2016 - Mar 2019) • Inventory Control Analyst (Jan 2013 - Aug 2016) • Inventory Control Clerk (Feb 2010 - Dec 2012). Nearly a decade of experience in inventory management, logistics, and operational analysis.',
        image: {
          light: '/images/light/connect.svg',
          dark: '/images/dark/connect.svg'
        }
      }
    ]
  },
  projects: {
    title: '',
    description: t('home.projects.description'),
    items: [
      {
        title: t('home.projects.items.ids_starter.title'),
        description: t('home.projects.items.ids_starter.description'),
        period: 'Jun 2022 - Present',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-box'
      },
      {
        title: t('home.projects.items.sakti.title'),
        description: t('home.projects.items.sakti.description'),
        period: 'May 2024 - Jul 2025',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-fingerprint',
        image: '/images/projects/sakti.png'
      },
      {
        title: t('home.projects.items.folur.title'),
        description: t('home.projects.items.folur.description'),
        period: 'Jul 2024 - Oct 2024',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-globe',
      },
      {
        title: t('home.projects.items.tekmira.title'),
        description: t('home.projects.items.tekmira.description'),
        period: 'Dec 2023 - Mar 2024',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-flask-conical',
        image: '/images/projects/tekmira-uprof.png'
      },
      {
        title: t('home.projects.items.malaria.title'),
        description: t('home.projects.items.malaria.description'),
        period: 'Apr 2023 - Sep 2023',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-simple-icons-drupal',
        image: '/images/projects/malaria-web.png'
      },
      {
        title: t('home.projects.items.slide_babel.title'),
        description: t('home.projects.items.slide_babel.description'),
        period: 'Jul 2023 - Sep 2023',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-fish',
        image: '/images/projects/slide-babel.png'
      },
      {
        title: t('home.projects.items.rabbani.title'),
        description: t('home.projects.items.rabbani.description'),
        period: 'Nov 2022 - Jun 2023',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-shopping-bag',
        image: '/images/projects/rabbani.png'
      },
      {
        title: t('home.projects.items.clove.title'),
        description: t('home.projects.items.clove.description'),
        period: 'Jan 2023 - May 2023',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-bar-chart-3',
        image: '/images/projects/clove-analytics.png'
      },
      {
        title: t('home.projects.items.koni_atlet.title'),
        description: t('home.projects.items.koni_atlet.description'),
        period: 'Jun 2022 - May 2023',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-medal',
        image: '/images/projects/koni-jabar-atlet.png'
      },
      {
        title: t('home.projects.items.starsender.title'),
        description: t('home.projects.items.starsender.description'),
        period: 'Apr 2023 - Apr 2023',
        company: 'Freelance',
        icon: 'i-simple-icons-whatsapp',
        image: '/images/projects/starsender.png'
      },
      {
        title: t('home.projects.items.favori.title'),
        description: t('home.projects.items.favori.description'),
        period: 'Oct 2022 - Mar 2023',
        company: 'Inacookies',
        icon: 'i-lucide-layout',
        image: '/images/projects/favori-app.png'
      },
      {
        title: t('home.projects.items.mtre3.title'),
        description: t('home.projects.items.mtre3.description'),
        period: 'Jun 2022 - Mar 2023',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-sun'
      },
      {
        title: t('home.projects.items.koni_dashboard.title'),
        description: t('home.projects.items.koni_dashboard.description'),
        period: 'Jul 2022 - Nov 2022',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-layout-dashboard',
        image: '/images/projects/koni-jabar-dashboard.png'
      },
      {
        title: t('home.projects.items.koni_website.title'),
        description: t('home.projects.items.koni_website.description'),
        period: 'Jul 2022 - Nov 2022',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-monitor',
        image: '/images/projects/konijabar-website.png'
      },
      {
        title: t('home.projects.items.frozen_food.title'),
        description: t('home.projects.items.frozen_food.description'),
        period: 'Nov 2021 - Aug 2022',
        company: 'Ritel Makanan Beku',
        icon: 'i-lucide-snowflake'
      },
      {
        title: t('home.projects.items.undss.title'),
        description: t('home.projects.items.undss.description'),
        period: 'Jun 2022 - Jul 2022',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-shield-alert',
      },
      {
        title: t('home.projects.items.zafaa.title'),
        description: t('home.projects.items.zafaa.description'),
        period: 'Apr 2022 - Jun 2022',
        company: 'Ritel Makanan Beku',
        icon: 'i-lucide-shopping-cart'
      }
    ]
  },
  cta: {
    title: 'Let\'s Build Something <span class="text-primary">Together</span>',
    description: 'I believe in taking risks, conquering fear, and continuously learning. Whether you have a project in mind or just want to connect, I\'d love to hear from you.',
    links: [
      {
        label: 'Get in Touch',
        to: 'mailto:m.rheza.alfin@gmail.com',
        trailingIcon: 'i-lucide-mail'
      },
      {
        label: 'View GitHub',
        to: 'https://github.com/vheins',
        target: '_blank',
        variant: 'subtle',
        icon: 'i-simple-icons-github'
      }
    ]
  }
}))

useSeoMeta({
  title: 'Muhammad Rheza Alfin - Full-stack Developer & IT Consultant',
  ogTitle: 'Muhammad Rheza Alfin - Full-stack Developer & IT Consultant',
  description: page.value.description,
  ogDescription: page.value.description,
  ogImage: 'https://ui.nuxt.com/assets/templates/nuxt/landing-light.png',
  twitterImage: 'https://ui.nuxt.com/assets/templates/nuxt/landing-light.png',
  twitterCard: 'summary_large_image'
})

const favoriteStack = [
  { name: 'Laravel', icon: 'i-simple-icons-laravel', color: 'hover:text-[#FF2D20]' },
  { name: 'Vue.js', icon: 'i-simple-icons-vuedotjs', color: 'hover:text-[#4FC08D]' },
  { name: 'PostgreSQL', icon: 'i-simple-icons-postgresql', color: 'hover:text-[#4169E1]' },
  { name: 'Redis', icon: 'i-simple-icons-redis', color: 'hover:text-[#DC382D]' },
  { name: 'Nginx', icon: 'i-simple-icons-nginx', color: 'hover:text-[#009639]' },
  { name: 'Debian', icon: 'i-simple-icons-debian', color: 'hover:text-[#E95420]' }
]

const otherStack = [
  { name: 'PHP', icon: 'i-simple-icons-php', color: 'hover:text-[#777BB4]' },
  { name: 'NestJS', icon: 'i-simple-icons-nestjs', color: 'hover:text-[#E0234E]' },
  { name: 'Node.js', icon: 'i-simple-icons-nodedotjs', color: 'hover:text-[#339933]' },
  { name: 'Python', icon: 'i-simple-icons-python', color: 'hover:text-[#3776AB]' },
  { name: 'Nuxt', icon: 'i-simple-icons-nuxtdotjs', color: 'hover:text-[#00DC82]' },
  { name: 'Vite', icon: 'i-simple-icons-vite', color: 'hover:text-[#646CFF]' },
  { name: 'UIkit', icon: 'i-simple-icons-uikit', color: 'hover:text-[#2396F3]' },
  { name: 'Tailwind CSS', icon: 'i-simple-icons-tailwindcss', color: 'hover:text-[#06B6D4]' },
  { name: 'Sass', icon: 'i-simple-icons-sass', color: 'hover:text-[#CC6699]' },
  { name: 'Pinia', icon: 'i-simple-icons-pinia', color: 'hover:text-[#FFD11B]' },
  { name: 'Axios', icon: 'i-simple-icons-axios', color: 'hover:text-[#5A29E4]' },
  { name: 'MySQL', icon: 'i-simple-icons-mysql', color: 'hover:text-[#4479A1]' },
  { name: 'Docker', icon: 'i-simple-icons-docker', color: 'hover:text-[#2496ED]' },
  { name: 'Odoo', icon: 'i-simple-icons-odoo', color: 'hover:text-[#714B67]' },
  { name: 'Sentry', icon: 'i-simple-icons-sentry', color: 'hover:text-[#362D59]' },
  { name: 'Pusher', icon: 'i-simple-icons-pusher', color: 'hover:text-[#300D4F]' },
  { name: 'Leaflet', icon: 'i-simple-icons-leaflet', color: 'hover:text-[#199900]' },
  { name: 'D3.js', icon: 'i-simple-icons-d3dotjs', color: 'hover:text-[#F9A03C]' },
  { name: 'JWT', icon: 'i-simple-icons-jsonwebtokens', color: 'hover:text-black dark:hover:text-white' }
]
</script>

<template>
  <div class="relative">
    <div class="hidden lg:block">
      <UColorModeImage light="/images/light/line-1.svg" dark="/images/dark/line-1.svg"
        class="absolute pointer-events-none pb-10 left-0 top-0 object-cover h-[650px]" />
    </div>

    <UPageHero :description="page.description" :links="page.hero.links" :ui="{
      container: 'md:pt-18 lg:pt-20',
      title: 'max-w-3xl mx-auto'
    }">
      <template #top>
        <HeroBackground />
      </template>

      <template #title>
        <span>
          {{ t('home.title_prefix') }} <span class="text-primary">{{ t('home.title_highlight') }}</span>
          {{ t('home.title_suffix') }}
        </span>
      </template>
    </UPageHero>

    <UContainer class="py-8 lg:py-16">
      <div class="flex flex-col items-center gap-12">
        <!-- Favorite Stack -->
        <div class="flex flex-col items-center gap-6">
          <p class="text-sm font-semibold text-primary uppercase tracking-wider">
            {{ t('home.stack.core') }}
          </p>
          <div class="flex flex-wrap justify-center gap-6 lg:gap-8 max-w-4xl">
            <UTooltip v-for="tech in favoriteStack" :key="tech.name" :text="tech.name">
              <div
                class="flex items-center justify-center p-4 rounded-2xl bg-primary/5 dark:bg-primary/10 ring-2 ring-primary/50 dark:ring-primary/50 shadow-lg shadow-primary/10 hover:scale-110 transition-all duration-300 group">
                <UIcon :name="tech.icon"
                  class="w-10 h-10 text-gray-500 dark:text-gray-400 transition-colors duration-200"
                  :class="tech.color" />
              </div>
            </UTooltip>
          </div>
        </div>

        <!-- Other Stack -->
        <div class="flex flex-col items-center gap-6">
          <p class="text-xs font-medium text-gray-400 dark:text-gray-500 uppercase tracking-wider">
            {{ t('home.stack.other') }}
          </p>
          <div class="flex flex-wrap justify-center gap-3 lg:gap-4 max-w-4xl">
            <UTooltip v-for="tech in otherStack" :key="tech.name" :text="tech.name">
              <div
                class="flex items-center justify-center p-2.5 rounded-xl bg-gray-50 dark:bg-gray-800/50 hover:bg-gray-100 dark:hover:bg-gray-800 transition-all duration-200 group ring-1 ring-gray-200 dark:ring-gray-800 hover:ring-primary/50 dark:hover:ring-primary/50">
                <UIcon :name="tech.icon" class="w-6 h-6 text-gray-400 dark:text-gray-500 transition-colors duration-200"
                  :class="tech.color" />
              </div>
            </UTooltip>
          </div>
        </div>
      </div>
    </UContainer>

    <UPageSection :description="page.section.description" :features="page.section.features" orientation="horizontal"
      :ui="{
        container: 'lg:px-0 2xl:px-20 mx-0 max-w-none md:mr-10',
        features: 'gap-0'
      }" reverse>
      <template #title>
        <span class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl">
          {{ t('home.transformation.title_prefix') }} <span
            class="text-primary">{{ t('home.transformation.title_highlight') }}</span>
          {{ t('home.transformation.title_suffix') }}
        </span>
      </template>
      <img :src="page.section.images.desktop" alt="Journey" class="hidden lg:block 2xl:hidden left-0 w-full max-w-2xl">
      <img :src="page.section.images.mobile" alt="Journey" class="block lg:hidden 2xl:block 2xl:w-full 2xl:max-w-2xl">
    </UPageSection>

    <USeparator :ui="{ border: 'border-primary/30' }" />

    <UPageSection id="features" :description="page.features.description" :features="page.features.features" :ui="{
      title: 'text-left @container relative flex',
      description: 'text-left'
    }" class="relative overflow-hidden">
      <div class="absolute rounded-full -left-10 top-10 size-[300px] z-10 bg-primary opacity-30 blur-[200px]" />
      <div class="absolute rounded-full -right-10 -bottom-10 size-[300px] z-10 bg-primary opacity-30 blur-[200px]" />
      <template #title>
        <span class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl">
          {{ t('home.expertise.title_prefix') }} <span
            class="text-primary">{{ t('home.expertise.title_highlight') }}</span> {{ t('home.expertise.title_suffix') }}
        </span>
        <div class="hidden @min-[1020px]:block">
          <UColorModeImage light="/images/light/line-2.svg" dark="/images/dark/line-2.svg"
            class="absolute top-0 right-0 size-full transform scale-95 translate-x-[70%]" />
        </div>
      </template>
    </UPageSection>

    <USeparator :ui="{ border: 'border-primary/30' }" />

    <HomeJourney id="steps" />

    <UPageSection id="projects" class="mb-32 overflow-hidden" :title="page.projects.title"
      :description="page.projects.description"
      :ui="{ title: 'text-left @container relative', description: 'text-left' }">
      <template #title>
        <span class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl">
          {{ t('home.projects.title_prefix') }} <span
            class="text-primary">{{ t('home.projects.title_highlight') }}</span> {{ t('home.projects.title_suffix') }}
        </span>

        <div class="hidden @min-[1120px]:block">
          <UColorModeImage light="/images/light/line-4.svg" dark="/images/dark/line-4.svg"
            class="absolute top-0 right-0 size-full transform translate-x-[60%]" />
        </div>
      </template>

      <UPageGrid>
        <UPageCard v-for="(project, index) in page.projects.items" :key="index" :title="project.title"
          :description="project.description" :ui="{ header: { padding: 'p-0 sm:p-0' } }">
          <template #header>
            <img :src="project.image || '/images/projects/default.png'" :alt="project.title"
              class="w-full h-48 object-cover object-top">
          </template>
          <template #footer>
            <div class="flex flex-col gap-1 text-sm text-gray-500 dark:text-gray-400">
              <div class="flex items-center gap-2">
                <UIcon name="i-lucide-calendar" class="w-4 h-4" />
                <span>{{ project.period }}</span>
              </div>
              <div class="flex items-center gap-2">
                <UIcon name="i-lucide-building-2" class="w-4 h-4" />
                <span>{{ project.company }}</span>
              </div>
            </div>
          </template>
        </UPageCard>
      </UPageGrid>
    </UPageSection>

    <AppCTA />
  </div>
</template>
