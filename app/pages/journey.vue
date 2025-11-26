<script setup lang="ts">
const experience = [
  {
    company: 'PT. Inovasi Dinamika Solusi',
    location: 'Bandung, West Java, Indonesia',
    type: 'Full-time',
    period: 'Jun 2022 - Present',
    roles: [
      {
        title: 'Software Development Team Lead',
        period: 'Jan 2023 - Present',
        description: 'Leading the software development team, managing project timelines, and overseeing the delivery of enterprise solutions.'
      },
      {
        title: 'Full-stack Developer',
        period: 'Jun 2022 - Jan 2023',
        description: 'Developed and maintained full-stack applications using Laravel, Vue.js, and Docker.'
      }
    ],
    icon: 'i-lucide-briefcase'
  },
  {
    company: 'Ritel Makanan Beku',
    location: 'Bandung, West Java, Indonesia',
    type: 'Full-time',
    period: 'Oct 2021 - Jun 2022',
    roles: [
      {
        title: 'Full-stack Developer',
        period: 'Oct 2021 - Jun 2022',
        description: 'Built comprehensive e-commerce and POS systems, managing the full development lifecycle.'
      }
    ],
    icon: 'i-lucide-snowflake'
  },
  {
    company: 'PT. Favori Corp Sedaya',
    location: 'Bandung, West Java, Indonesia',
    type: 'Full-time',
    period: 'Aug 2020 - Oct 2021',
    roles: [
      {
        title: 'Head Of Sales Operations',
        period: 'Aug 2020 - Oct 2021',
        description: 'Managed sales operations, optimized processes, and oversaw team performance.'
      }
    ],
    icon: 'i-lucide-trending-up'
  },
  {
    company: 'Indomaret Group',
    location: 'Bandung, West Java, Indonesia',
    type: 'Full-time',
    period: 'Feb 2010 - Mar 2019',
    roles: [
      {
        title: 'Inventory Control Supervisor',
        period: 'Aug 2016 - Mar 2019',
        description: 'Supervised inventory control operations, ensuring accuracy and efficiency in stock management.'
      },
      {
        title: 'Inventory Control Analyst',
        period: 'Jan 2013 - Aug 2016',
        description: 'Analyzed inventory data to identify trends, discrepancies, and opportunities for improvement.'
      },
      {
        title: 'Inventory Control Clerk',
        period: 'Feb 2010 - Dec 2012',
        description: 'Performed daily inventory checks and maintained accurate stock records.'
      }
    ],
    icon: 'i-lucide-store'
  }
]

useSeoMeta({
  title: 'Journey - Muhammad Rheza Alfin',
  description: 'My professional journey and career milestones.'
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
      title="Professional Journey"
      description="A timeline of my career path, key roles, and significant milestones."
      align="center"
      :links="links"
    >
      <template #top>
        <HeroBackground />
      </template>
    </UPageHero>

    <UContainer class="mt-24">
      <div class="relative max-w-4xl mx-auto pb-24">
        <!-- Vertical Line -->
        <div
          class="absolute left-4 md:left-1/2 top-0 bottom-0 w-px bg-gray-200 dark:bg-gray-800 transform md:-translate-x-1/2"
        />

        <div class="space-y-12">
          <div
            v-for="(item, index) in experience"
            :key="index"
            class="relative flex flex-col md:flex-row gap-8 md:gap-0 group"
          >
            <!-- Date (Left/Right alternating) -->
            <div
              class="md:w-1/2 flex items-center"
              :class="[index % 2 === 0 ? 'md:justify-end md:pr-12 md:text-right' : 'md:order-2 md:justify-start md:pl-12 md:text-left']"
            >
              <div class="ml-12 md:ml-0">
                <span class="text-primary font-bold text-lg block">{{ item.period }}</span>
                <span class="text-gray-900 dark:text-white font-bold text-xl block mt-1">{{ item.company }}</span>
                <div class="text-sm text-gray-500 dark:text-gray-400 mt-1">
                  <span>{{ item.location }}</span>
                  <span class="mx-1">·</span>
                  <span>{{ item.type }}</span>
                </div>
              </div>
            </div>

            <!-- Timeline Node -->
            <div
              class="absolute left-4 md:left-1/2 w-8 h-8 rounded-full border-4 border-white dark:border-gray-900 bg-primary transform -translate-x-1/2 flex items-center justify-center z-10 shadow-md group-hover:scale-110 transition-transform duration-300"
            >
              <UIcon
                :name="item.icon"
                class="w-4 h-4 text-white"
              />
            </div>

            <!-- Content Card (Right/Left alternating) -->
            <div
              class="md:w-1/2 ml-12 md:ml-0"
              :class="[index % 2 === 0 ? 'md:order-2 md:pl-12' : 'md:pr-12']"
            >
              <div
                class="p-6 bg-gray-50 dark:bg-gray-800/50 rounded-xl border border-gray-200 dark:border-gray-800 hover:border-primary/50 dark:hover:border-primary/50 transition-colors duration-300"
              >
                <div class="space-y-6">
                  <div
                    v-for="(role, roleIndex) in item.roles"
                    :key="roleIndex"
                    class="relative pl-4 border-l-2 border-gray-200 dark:border-gray-700 last:border-0"
                  >
                    <div class="absolute -left-[5px] top-2 w-2 h-2 rounded-full bg-gray-300 dark:bg-gray-600" />
                    <h3 class="text-lg font-bold text-gray-900 dark:text-white">
                      {{ role.title }}
                    </h3>
                    <p class="text-sm text-primary font-medium mb-2">
                      {{ role.period }}
                    </p>
                    <p class="text-gray-600 dark:text-gray-300 text-sm">
                      {{ role.description }}
                    </p>
                  </div>
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
