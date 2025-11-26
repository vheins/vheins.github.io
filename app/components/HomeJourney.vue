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
    icon: 'i-lucide-briefcase',
    color: 'bg-blue-50 dark:bg-blue-900/20 text-blue-500'
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
    icon: 'i-lucide-snowflake',
    color: 'bg-cyan-50 dark:bg-cyan-900/20 text-cyan-500'
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
    icon: 'i-lucide-trending-up',
    color: 'bg-orange-50 dark:bg-orange-900/20 text-orange-500'
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
    icon: 'i-lucide-store',
    color: 'bg-red-50 dark:bg-red-900/20 text-red-500'
  }
]
</script>

<template>
  <div class="py-16 md:py-24 relative overflow-hidden">
    <div class="text-center mb-16 relative z-10">
      <h2 class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl mb-4">
        My <span class="text-primary">Journey</span>
      </h2>
      <p class="text-lg text-gray-600 dark:text-gray-400 max-w-2xl mx-auto">
        From inventory control to cloud infrastructure - every step has built who I am today.
      </p>
    </div>

    <!-- Horizontal Scroll Container -->
    <div class="relative px-4 md:px-8 lg:px-16">
      <!-- Connecting Line -->
      <div
        class="absolute top-1/2 left-0 w-full h-1 bg-gray-200 dark:bg-gray-800 -translate-y-1/2 hidden md:block"
      />

      <div class="flex overflow-x-auto pb-12 gap-12 snap-x snap-mandatory hide-scrollbar pt-8">
        <div
          v-for="(item, index) in experience"
          :key="index"
          class="flex-shrink-0 w-[300px] snap-center relative group"
        >
          <!-- Content (Top) -->
          <div class="mb-8 relative">
            <div
              class="bg-white dark:bg-gray-800/50 p-6 rounded-xl border border-gray-200 dark:border-gray-800 hover:border-primary/50 dark:hover:border-primary/50 transition-all duration-300 shadow-sm group-hover:shadow-md h-[280px] flex flex-col"
            >
              <h3
                class="text-lg font-bold text-gray-900 dark:text-white mb-1 line-clamp-1"
                :title="item.company"
              >
                {{ item.company }}
              </h3>
              <p class="text-sm text-gray-500 dark:text-gray-400 mb-4">
                {{ item.location }}
              </p>

              <div class="space-y-4 overflow-y-auto flex-1 pr-2 custom-scrollbar">
                <div
                  v-for="(role, roleIndex) in item.roles"
                  :key="roleIndex"
                  class="relative pl-3 border-l-2 border-gray-100 dark:border-gray-700"
                >
                  <h4 class="font-bold text-sm text-gray-900 dark:text-white">
                    {{ role.title }}
                  </h4>
                  <p class="text-xs text-primary font-medium mb-1">
                    {{ role.period }}
                  </p>
                  <p class="text-xs text-gray-600 dark:text-gray-300 line-clamp-3">
                    {{ role.description }}
                  </p>
                </div>
              </div>

              <!-- Arrow pointing down -->
              <div
                class="absolute -bottom-2 left-1/2 -translate-x-1/2 w-4 h-4 bg-white dark:bg-gray-800 border-b border-r border-gray-200 dark:border-gray-800 transform rotate-45 group-hover:border-primary/50 dark:group-hover:border-primary/50 transition-colors duration-300"
              />
            </div>
          </div>

          <!-- Icon Circle (Middle) -->
          <div class="relative flex justify-center items-center z-10 mb-4">
            <div
              class="w-16 h-16 rounded-full bg-white dark:bg-gray-900 border-4 border-gray-100 dark:border-gray-800 flex items-center justify-center group-hover:scale-110 group-hover:border-primary transition-all duration-300 shadow-sm"
            >
              <UIcon
                :name="item.icon"
                class="w-8 h-8 text-gray-400 group-hover:text-primary transition-colors duration-300"
              />
            </div>
          </div>

          <!-- Date (Bottom) -->
          <div class="text-center">
            <span
              class="text-2xl font-bold text-gray-900 dark:text-white block"
            >{{ item.period.split(' - ')[0].split(' ')[1] }}</span>
            <span class="text-sm text-gray-500 dark:text-gray-400">{{ item.period }}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hide-scrollbar::-webkit-scrollbar {
    display: none;
}

.hide-scrollbar {
    -ms-overflow-style: none;
    scrollbar-width: none;
}

.custom-scrollbar::-webkit-scrollbar {
    width: 4px;
}

.custom-scrollbar::-webkit-scrollbar-track {
    background: transparent;
}

.custom-scrollbar::-webkit-scrollbar-thumb {
    background-color: rgba(156, 163, 175, 0.5);
    border-radius: 20px;
}
</style>
