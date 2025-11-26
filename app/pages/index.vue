<script setup lang="ts">
const page = {
  title: 'From Retail Floors to <span class="text-primary">Cloud Servers</span>',
  description: 'Full-stack Developer & IT Consultant specializing in performance tuning, system integration, and automation. I combine business operations knowledge with technology to deliver solutions that improve real-world processes.',
  hero: {
    links: [
      {
        label: 'View Projects',
        icon: 'i-lucide-folder-git-2',
        trailing: true,
        color: 'primary',
        to: '#projects',
        size: 'xl'
      },
      {
        label: 'GitHub',
        icon: 'i-simple-icons-github',
        size: 'xl',
        color: 'neutral',
        variant: 'outline',
        to: 'https://github.com/vheins',
        target: '_blank'
      }
    ]
  },
  section: {
    title: 'A Journey of <span class="text-primary">Transformation</span>',
    description: 'Nearly a decade in retail operations taught me to think analytically, pay attention to detail, and focus on preventing errors and inefficiencies. Today, I apply these same principles to software development.',
    images: {
      mobile: '/images/journey-professional.png',
      desktop: '/images/journey-professional.png'
    },
    features: [
      {
        title: 'Analytical Thinking',
        description: 'Trained through years of investigating irregularities and operational misuse at Indomaret Group. I approach every problem systematically, identifying root causes and implementing preventive solutions.',
        class: 'border-l border-primary pl-4'
      },
      {
        title: 'Attention to Detail',
        description: 'From managing inventory accuracy across multiple stores to writing clean, maintainable code - precision matters. Every line of code, every configuration, every deployment is carefully considered.',
        class: 'border-l border-default pt-4 pl-4'
      },
      {
        title: 'Process Improvement',
        description: 'Whether optimizing stock reporting workflows or architecting scalable systems, I\'m driven by efficiency. I believe technology should solve real problems and improve real processes.',
        class: 'border-l border-default pt-4 pl-4'
      }
    ]
  },
  features: {
    title: 'Technical <span class="text-primary">Expertise</span>',
    description: 'Building modern, scalable solutions with a focus on performance, maintainability, and real-world impact.',
    features: [
      {
        title: 'Backend Development',
        description: 'Laravel and NestJS frameworks with PostgreSQL, MySQL, and Redis for robust, high-performance applications.',
        icon: 'i-lucide-server',
        ui: { leading: 'bg-accented/50 p-2 rounded-md border border-muted border-dashed' }
      },
      {
        title: 'Frontend Development',
        description: 'Vue.js, Nuxt, and Next.js for building clean, reactive user interfaces with modern JavaScript best practices.',
        icon: 'i-lucide-layout-dashboard',
        ui: { leading: 'bg-accented/50 p-2 rounded-md border border-muted border-dashed' }
      },
      {
        title: 'Performance Optimization',
        description: 'Leveraging Soketi, Octane, and Redis for real-time features and blazing-fast response times.',
        icon: 'i-lucide-zap',
        ui: { leading: 'bg-accented/50 p-2 rounded-md border border-muted border-dashed' }
      },
      {
        title: 'DevOps & Infrastructure',
        description: 'Docker, Nginx, Kong, HAProxy, and Patroni for scalable, reliable deployments and high availability.',
        icon: 'i-lucide-cloud',
        ui: { leading: 'bg-accented/50 p-2 rounded-md border border-muted border-dashed' }
      },
      {
        title: 'Enterprise Integration',
        description: 'ERP systems integration with Odoo, building bridges between business operations and technology.',
        icon: 'i-lucide-workflow',
        ui: { leading: 'bg-accented/50 p-2 rounded-md border border-muted border-dashed' }
      },
      {
        title: 'Team Leadership',
        description: 'Leading development teams, mentoring developers, and fostering a culture of continuous learning and excellence.',
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
    title: 'Featured <span class="text-primary">Projects</span>',
    description: 'A comprehensive list of projects I have delivered, ranging from enterprise resource planning to specialized dashboards and e-commerce platforms.',
    items: [
      {
        title: 'IDS Starter Kit',
        description: 'The FullStack Application Starter Kit utilizes the Laravel framework, VueJS, UI Kit, and is Docker-friendly. This comprehensive starter kit provides developers with a solid foundation to kickstart full-stack application development.',
        period: 'Jun 2022 - Present',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-box'
      },
      {
        title: 'Sistem Absensi dan Laporan Terintegrasi (Sakti)',
        description: 'Designed for PT Pesonna Optima Jasa to manage employee attendance records, utilizing technologies like DeepFace for facial recognition to ensure accurate clock-in/out procedures and generating integrated reports.',
        period: 'May 2024 - Jul 2025',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-fingerprint',
        image: '/images/projects/sakti.png'
      },
      {
        title: 'Folur Global Platform',
        description: 'The Food Systems, Land Use, and Restoration (FOLUR) initiative aims to transform agricultural practices and land use to support sustainability, food security, and the restoration of agricultural lands across 27 countries.',
        period: 'Jul 2024 - Oct 2024',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-globe',
        image: '/images/projects/folur-web.png'
      },
      {
        title: 'tekMIRA-Uji Profisiensi',
        description: 'Proficiency testing program to evaluate the performance of participant laboratories in testing coal, coal ash, laterite nickel minerals, bauxite, and iron ore, ensuring compliance with ISO 17025 standards.',
        period: 'Dec 2023 - Mar 2024',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-flask-conical',
        image: '/images/projects/tekmira-uprof.png'
      },
      {
        title: 'Malaria Website with Drupal 9.5',
        description: 'Developed for UNDP HEART Program to support national efforts in addressing health inequality. Focuses on strengthening the Global Fund for AIDS, Tuberculosis and Malaria (GFATM) Country Coordinating Mechanisms.',
        period: 'Apr 2023 - Sep 2023',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-simple-icons-drupal',
        image: '/images/projects/malaria-web.png'
      },
      {
        title: 'Slide Babel - Sistem Informasi Perikanan',
        description: 'Fisheries information services platform providing data on Fish Price, Availability, Cultivated Fish Types, Marketing Locations, and Cold Storage Facilities for the Marine and Fisheries Service of Bangka Belitung Province.',
        period: 'Jul 2023 - Sep 2023',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-fish',
        image: '/images/projects/slide-babel.png'
      },
      {
        title: 'Rabbani Web Commerce',
        description: 'E-commerce platform specializing in Islamic-based products. Designed to provide a convenient and secure shopping experience with features aligning with Islamic values and ethical production practices.',
        period: 'Nov 2022 - Jun 2023',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-shopping-bag',
        image: '/images/projects/rabbani.png'
      },
      {
        title: 'Clove Analytics Dashboard',
        description: 'Website Analytic Tool for Clove statistical Research. Features User/Role Management, Subscription Management, and specific statistical modules like Significant Test, Proportion Test, and Brand Maps.',
        period: 'Jan 2023 - May 2023',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-bar-chart-3',
        image: '/images/projects/clove-analytics.png'
      },
      {
        title: 'Koni Jabar Atlet Management',
        description: 'Platform integrating athlete data, training programs, and sports achievements in West Java. A comprehensive source of information for tracking athletes and coaching programs.',
        period: 'Jun 2022 - May 2023',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-medal',
        image: '/images/projects/koni-jabar-atlet.png'
      },
      {
        title: 'Starsender Plugin for WHMCS',
        description: 'Seamless integration of WhatsApp API into the WHMCS platform. Enables sending WhatsApp messages directly from the WHMCS dashboard for efficient client communication.',
        period: 'Apr 2023 - Apr 2023',
        company: 'Freelance',
        icon: 'i-simple-icons-whatsapp',
        image: '/images/projects/starsender.png'
      },
      {
        title: 'Favori App V2',
        description: 'Information system dashboard for Inacookies internal use. Allows monitoring of sales data, production metrics, inventory levels, and customer feedback with real-time visualization.',
        period: 'Oct 2022 - Mar 2023',
        company: 'Inacookies',
        icon: 'i-lucide-layout',
        image: '/images/projects/favori-app.png'
      },
      {
        title: 'MTRE3 Insentif Surya Atap',
        description: 'Online platform for Roof Solar Power Incentive (PLTS Atap) grant applications, provided by the Sustainable Energy Fund (SEF) under the MTRE3 project (UNDP & Govt of Indonesia).',
        period: 'Jun 2022 - Mar 2023',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-sun'
      },
      {
        title: 'Koni Jabar Dashboard',
        description: 'Dashboard for West Java Sports Resource Data Center. Provides interactive visualizations regarding athletes, training programs, and sporting achievements.',
        period: 'Jul 2022 - Nov 2022',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-layout-dashboard',
        image: '/images/projects/koni-jabar-dashboard.png'
      },
      {
        title: 'Koni Jabar Website',
        description: 'Maintenance, feature enhancements, and bug fixing for the Koni Jabar website to ensure optimal performance and improved user experience.',
        period: 'Jul 2022 - Nov 2022',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-monitor',
        image: '/images/projects/konijabar-website.png'
      },
      {
        title: 'Frozen Food Dashboard & E-Commerce',
        description: 'Comprehensive system combining e-commerce, warehousing, purchasing, and stocktaking capabilities. Streamlines operations and manages inventory for frozen food retail.',
        period: 'Nov 2021 - Aug 2022',
        company: 'Ritel Makanan Beku',
        icon: 'i-lucide-snowflake'
      },
      {
        title: 'UNDSS Dashboard',
        description: 'Bug fixing and new feature development for UNDSS Dashboard. Processes incident data into a centralized bank for spatial analysis and risk management.',
        period: 'Jun 2022 - Jul 2022',
        company: 'PT. Inovasi Dinamika Solusi',
        icon: 'i-lucide-shield-alert',
        image: '/images/projects/undss-dashboard.png'
      },
      {
        title: 'Zafaa POS',
        description: 'Specialized POS application for frozen food retail. Features stock monitoring, card payment integration, and customer management to improve retail efficiency.',
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
}

useSeoMeta({
  title: 'Muhammad Rheza Alfin - Full-stack Developer & IT Consultant',
  ogTitle: 'Muhammad Rheza Alfin - Full-stack Developer & IT Consultant',
  description: page.description,
  ogDescription: page.description,
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
      <UColorModeImage
        light="/images/light/line-1.svg"
        dark="/images/dark/line-1.svg"
        class="absolute pointer-events-none pb-10 left-0 top-0 object-cover h-[650px]"
      />
    </div>

    <UPageHero
      :description="page.description"
      :links="page.hero.links"
      :ui="{
        container: 'md:pt-18 lg:pt-20',
        title: 'max-w-3xl mx-auto'
      }"
    >
      <template #top>
        <HeroBackground />
      </template>

      <template #title>
        <span v-html="page.title" />
      </template>
    </UPageHero>

    <UContainer class="py-8 lg:py-16">
      <div class="flex flex-col items-center gap-12">
        <!-- Favorite Stack -->
        <div class="flex flex-col items-center gap-6">
          <p class="text-sm font-semibold text-primary uppercase tracking-wider">
            My Core Stack
          </p>
          <div class="flex flex-wrap justify-center gap-6 lg:gap-8 max-w-4xl">
            <UTooltip
              v-for="tech in favoriteStack"
              :key="tech.name"
              :text="tech.name"
            >
              <div
                class="flex items-center justify-center p-4 rounded-2xl bg-primary/5 dark:bg-primary/10 ring-2 ring-primary/50 dark:ring-primary/50 shadow-lg shadow-primary/10 hover:scale-110 transition-all duration-300 group"
              >
                <UIcon
                  :name="tech.icon"
                  class="w-10 h-10 text-gray-500 dark:text-gray-400 transition-colors duration-200"
                  :class="tech.color"
                />
              </div>
            </UTooltip>
          </div>
        </div>

        <!-- Other Stack -->
        <div class="flex flex-col items-center gap-6">
          <p class="text-xs font-medium text-gray-400 dark:text-gray-500 uppercase tracking-wider">
            Other Technologies I
            Use
          </p>
          <div class="flex flex-wrap justify-center gap-3 lg:gap-4 max-w-4xl">
            <UTooltip
              v-for="tech in otherStack"
              :key="tech.name"
              :text="tech.name"
            >
              <div
                class="flex items-center justify-center p-2.5 rounded-xl bg-gray-50 dark:bg-gray-800/50 hover:bg-gray-100 dark:hover:bg-gray-800 transition-all duration-200 group ring-1 ring-gray-200 dark:ring-gray-800 hover:ring-primary/50 dark:hover:ring-primary/50"
              >
                <UIcon
                  :name="tech.icon"
                  class="w-6 h-6 text-gray-400 dark:text-gray-500 transition-colors duration-200"
                  :class="tech.color"
                />
              </div>
            </UTooltip>
          </div>
        </div>
      </div>
    </UContainer>

    <UPageSection
      :description="page.section.description"
      :features="page.section.features"
      orientation="horizontal"
      :ui="{
        container: 'lg:px-0 2xl:px-20 mx-0 max-w-none md:mr-10',
        features: 'gap-0'
      }"
      reverse
    >
      <template #title>
        <span
          class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl"
          v-html="page.section.title"
        />
      </template>
      <img
        :src="page.section.images.desktop"
        alt="Journey"
        class="hidden lg:block 2xl:hidden left-0 w-full max-w-2xl"
      >
      <img
        :src="page.section.images.mobile"
        alt="Journey"
        class="block lg:hidden 2xl:block 2xl:w-full 2xl:max-w-2xl"
      >
    </UPageSection>

    <USeparator :ui="{ border: 'border-primary/30' }" />

    <UPageSection
      id="features"
      :description="page.features.description"
      :features="page.features.features"
      :ui="{
        title: 'text-left @container relative flex',
        description: 'text-left'
      }"
      class="relative overflow-hidden"
    >
      <div class="absolute rounded-full -left-10 top-10 size-[300px] z-10 bg-primary opacity-30 blur-[200px]" />
      <div class="absolute rounded-full -right-10 -bottom-10 size-[300px] z-10 bg-primary opacity-30 blur-[200px]" />
      <template #title>
        <span
          class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl"
          v-html="page.features.title"
        />
        <div class="hidden @min-[1020px]:block">
          <UColorModeImage
            light="/images/light/line-2.svg"
            dark="/images/dark/line-2.svg"
            class="absolute top-0 right-0 size-full transform scale-95 translate-x-[70%]"
          />
        </div>
      </template>
    </UPageSection>

    <USeparator :ui="{ border: 'border-primary/30' }" />

    <HomeJourney id="steps" />

    <UPageSection
      id="projects"
      class="mb-32 overflow-hidden"
      :title="page.projects.title"
      :description="page.projects.description"
      :ui="{ title: 'text-left @container relative', description: 'text-left' }"
    >
      <template #title>
        <span
          class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl"
          v-html="page.projects.title"
        />

        <div class="hidden @min-[1120px]:block">
          <UColorModeImage
            light="/images/light/line-4.svg"
            dark="/images/dark/line-4.svg"
            class="absolute top-0 right-0 size-full transform translate-x-[60%]"
          />
        </div>
      </template>

      <UPageGrid>
        <UPageCard
          v-for="(project, index) in page.projects.items"
          :key="index"
          :title="project.title"
          :description="project.description"
          :ui="{ header: { padding: 'p-0 sm:p-0' } }"
        >
          <template #header>
            <img
              :src="project.image || '/images/projects/default.png'"
              :alt="project.title"
              class="w-full h-48 object-cover object-top"
            >
          </template>
          <template #footer>
            <div class="flex flex-col gap-1 text-sm text-gray-500 dark:text-gray-400">
              <div class="flex items-center gap-2">
                <UIcon
                  name="i-lucide-calendar"
                  class="w-4 h-4"
                />
                <span>{{ project.period }}</span>
              </div>
              <div class="flex items-center gap-2">
                <UIcon
                  name="i-lucide-building-2"
                  class="w-4 h-4"
                />
                <span>{{ project.company }}</span>
              </div>
            </div>
          </template>
        </UPageCard>
      </UPageGrid>
    </UPageSection>

    <USeparator />

    <UPageCTA
      v-bind="page.cta"
      variant="naked"
      class="overflow-hidden @container"
    >
      <template #title>
        <span
          class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl"
          v-html="page.cta.title"
        />

        <div class="@max-[1280px]:hidden">
          <UColorModeImage
            light="/images/light/line-6.svg"
            dark="/images/dark/line-6.svg"
            class="absolute left-10 -top-10 sm:top-0 h-full"
          />
          <UColorModeImage
            light="/images/light/line-7.svg"
            dark="/images/dark/line-7.svg"
            class="absolute right-0 bottom-0 h-full"
          />
        </div>
      </template>

      <LazyStarsBg />
    </UPageCTA>
  </div>
</template>
