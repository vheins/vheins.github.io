<script setup lang="ts">
const page = {
  title: 'From Retail Floors to <span class="text-primary">Cloud Servers</span>',
  description: 'Full-stack Developer & Team Lead specializing in Laravel, Vue.js, and scalable architectures. I combine business operations knowledge with technology to deliver solutions that improve real-world processes.',
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
      mobile: '/images/macbook-mobile.svg',
      desktop: '/images/macbook.svg'
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
        description: 'Laravel framework with PostgreSQL, MySQL, and Redis for robust, high-performance applications.',
        icon: 'i-lucide-server',
        ui: { leading: 'bg-accented/50 p-2 rounded-md border border-muted border-dashed' }
      },
      {
        title: 'Frontend Development',
        description: 'Vue.js for building clean, reactive user interfaces with modern JavaScript best practices.',
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
    description: 'A selection of projects showcasing enterprise solutions, integrations, and innovative applications.',
    plans: [
      {
        title: 'ERP Integration Platform',
        description: 'Seamless integration with Odoo ERP system for enterprise resource planning.',
        price: 'Enterprise',
        features: [
          'Laravel backend with PostgreSQL database',
          'Real-time data synchronization with Soketi',
          'Vue.js dashboard for monitoring and control',
          'Docker containerization for easy deployment',
          'RESTful API with comprehensive documentation',
          'Automated testing and CI/CD pipeline'
        ],
        button: {
          label: 'View Details',
          color: 'neutral',
          variant: 'outline',
          to: '#'
        }
      },
      {
        title: 'AI-Driven Dashboard',
        description: 'Intelligent analytics platform with AI-powered insights and predictions.',
        price: 'Innovation',
        highlight: true,
        features: [
          'Laravel Octane for high-performance API',
          'Vue.js with real-time data visualization',
          'Redis caching for optimal performance',
          'PostgreSQL with advanced analytics queries',
          'Machine learning integration',
          'Responsive design for all devices'
        ],
        button: {
          label: 'View Details',
          variant: 'subtle',
          to: '#'
        }
      },
      {
        title: 'Scalable Infrastructure',
        description: 'High-availability deployment architecture for mission-critical applications.',
        price: 'DevOps',
        features: [
          'Docker containerization and orchestration',
          'Nginx reverse proxy with load balancing',
          'Kong API gateway for microservices',
          'HAProxy for high availability',
          'Patroni for PostgreSQL clustering',
          'Automated monitoring and alerting'
        ],
        button: {
          label: 'View Details',
          color: 'neutral',
          variant: 'outline',
          to: '#'
        }
      }
    ]
  },
  cta: {
    title: 'Let\'s Build Something <span class="text-primary">Together</span>',
    description: 'I believe in taking risks, conquering fear, and continuously learning. Whether you have a project in mind or just want to connect, I\'d love to hear from you.',
    links: [
      {
        label: 'Get in Touch',
        to: 'mailto:your.email@example.com',
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
  title: 'Vheins - Full-stack Developer & Team Lead',
  ogTitle: 'Vheins - Full-stack Developer & Team Lead',
  description: page.description,
  ogDescription: page.description,
  ogImage: 'https://ui.nuxt.com/assets/templates/nuxt/landing-light.png',
  twitterImage: 'https://ui.nuxt.com/assets/templates/nuxt/landing-light.png',
  twitterCard: 'summary_large_image'
})
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
        <span v-html="page.title" />
      </template>
    </UPageHero>

    <UPageSection :description="page.section.description" :features="page.section.features" orientation="horizontal"
      :ui="{
        container: 'lg:px-0 2xl:px-20 mx-0 max-w-none md:mr-10',
        features: 'gap-0'
      }" reverse>
      <template #title>
        <span v-html="page.section.title"
          class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl" />
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
        <span v-html="page.features.title"
          class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl" />
        <div class="hidden @min-[1020px]:block">
          <UColorModeImage light="/images/light/line-2.svg" dark="/images/dark/line-2.svg"
            class="absolute top-0 right-0 size-full transform scale-95 translate-x-[70%]" />
        </div>
      </template>
    </UPageSection>

    <USeparator :ui="{ border: 'border-primary/30' }" />

    <UPageSection id="steps" :description="page.steps.description" class="relative overflow-hidden">
      <template #headline>
        <UColorModeImage light="/images/light/line-3.svg" dark="/images/dark/line-3.svg"
          class="absolute -top-10 sm:top-0 right-1/2 h-24" />
      </template>
      <template #title>
        <span v-html="page.steps.title"
          class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl" />
      </template>

      <template #features>
        <UPageCard v-for="(step, index) in page.steps.items" :key="index" class="group"
          :ui="{ container: 'p-4 sm:p-4', title: 'flex items-center gap-1' }">
          <UColorModeImage v-if="step.image" :light="step.image?.light" :dark="step.image?.dark" :alt="step.title"
            class="size-full" />

          <div class="flex flex-col gap-2">
            <span class="text-lg font-semibold">
              {{ step.title }}
            </span>
            <span class="text-sm text-muted">
              {{ step.description }}
            </span>
          </div>
        </UPageCard>
      </template>
    </UPageSection>

    <UPageSection id="projects" class="mb-32 overflow-hidden" :title="page.projects.title"
      :description="page.projects.description" :plans="page.projects.plans"
      :ui="{ title: 'text-left @container relative', description: 'text-left' }">
      <template #title>
        <span v-html="page.projects.title"
          class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl" />

        <div class="hidden @min-[1120px]:block">
          <UColorModeImage light="/images/light/line-4.svg" dark="/images/dark/line-4.svg"
            class="absolute top-0 right-0 size-full transform translate-x-[60%]" />
        </div>
      </template>

      <UPricingPlans scale>
        <UPricingPlan v-for="(plan, index) in page.projects.plans" :key="index" :title="plan.title"
          :description="plan.description" :price="plan.price" :billing-period="plan.billing_period"
          :billing-cycle="plan.billing_cycle" :highlight="plan.highlight" :scale="plan.highlight" variant="soft"
          :features="plan.features" :button="plan.button" />
      </UPricingPlans>
    </UPageSection>

    <USeparator />

    <UPageCTA v-bind="page.cta" variant="naked" class="overflow-hidden @container">
      <template #title>
        <span v-html="page.cta.title"
          class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl" />

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
