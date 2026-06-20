<template>
    <header class="h-32 bg-neutral-100 w-full px-10 border-b-2">
      <div class="flex items-start justify-between">
        <div class="flex items-center gap-4">
            <div class="flex items-center gap-3 py-4">
                <a href="#" aria-label="Twitter" class="text-gray-600 hover:text-blue-500">
                    <NuxtIcon name="i-lucide-send" class="size-6" />
                </a>
                <a href="#" aria-label="Twitter" class="text-gray-600 hover:text-blue-500">
                    <NuxtIcon name="i-lucide-twitter" class="size-6" />
                </a>
                <a href="#" aria-label="GitHub" class="text-gray-600 hover:text-gray-900">
                    <NuxtIcon name="i-lucide-github" class="size-6" />
                </a>
                <a href="#" aria-label="Instagram" class="text-gray-600 hover:text-pink-500">
                    <NuxtIcon name="i-lucide-instagram" class="size-6" />
                </a>
            </div>
        </div>
        <div>
            <img src="/FE_logo1.png" alt="FE Logo" class="h-20 w-auto" />
        </div>
        <div class="py-4">
            <UButton size="md" variant="solid" class="text-gray-600 hover:text-red-900 cursor-pointer">
                <NuxtIcon name="i-lucide-search" class="size-6" />
            </UButton>
        </div>
      </div>
      <nav class="flex items-center justify-center">
        <NuxtNavigationMenu arrow content-orientation="vertical" :items="items" class="w-full justify-center" />
      </nav>
    </header>
    <slot />
</template>
<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'

const items = ref<NavigationMenuItem[]>([
  {
    label: 'Home',
    icon: 'i-lucide-home',
    to: '#'
  },
  {
    label: 'About',
    icon: 'i-lucide-info',
    to: '#',
    children: [
      {
        label: 'Faculty of Engineering',
        description: 'Learn about the Faculty of Engineering at our university.',
        icon: 'i-lucide-university',
        to: '#'
      },
      {
        label: 'Facilities',
        description: 'Explore the state-of-the-art facilities available to our students.',
        icon: 'i-lucide-building',
        to: '#'
      },
      {
        label: 'History',
        description: 'Discover the rich history and milestones of our Faculty of Engineering.',
        icon: 'i-lucide-clock',
        to: '#'
      },
      {
        label: 'Offices and Administration',
        description: 'Find information about our administrative offices and contact details.',
        icon: 'i-lucide-office-building',
        to: '#',
        children: [
          {
            label: 'Computer Science Department',
            description: 'Learn about the Computer Science Department and its offerings.',
            icon: 'i-lucide-desktop',
            to: '#'
          },
          {
            label: 'Mechanical Engineering Department',
            description: 'Discover the Mechanical Engineering Department and its programs.',
            icon: 'i-lucide-wrench',
            to: '#'
          },
          {
            label: 'Civil Engineering Department',
            description: 'Explore the Civil Engineering Department and its courses.',
            icon: 'i-lucide-building-2',
            to: '#'
          }
        ]
      },
      {
        label: 'Map and Location',
        description: 'Find our campus location and view the map.',
        icon: 'i-lucide-map-pin',
        to: '#'
      }
    ]
  },
  {
    label: 'Academics',
    icon: 'i-lucide-graduation-cap',
    to: '#',
    children: [
      {
        label: 'Degree Program',
        icon: 'i-lucide-folder',
        description: 'Browse degree programs and departments.',
        children: [
          {
            label: 'Computer Science Department',
            icon: 'i-lucide-desktop',
            description: 'BSc and MSc programs in Computer Science.',
            to: '#'
          },
          {
            label: 'Civil Engineering Department',
            icon: 'i-lucide-building-2',
            description: 'Undergraduate and postgraduate civil engineering programs.',
            to: '#'
          },
          {
            label: 'Mechanical Engineering Department',
            icon: 'i-lucide-wrench',
            description: 'Mechanical engineering degrees and research.',
            to: '#'
          }
        ]
      },
      {
        label: 'Academic Calendar',
        icon: 'i-lucide-calendar',
        description: 'Important academic dates and deadlines.',
        to: '#'
      }
    ]
  },
  {
    label: 'Admission',
    icon: 'i-lucide-user-plus',
    to: '#',
    children: [
      {
        label: 'Why choose VSU',
        icon: 'i-lucide-star',
        description: 'Reasons to choose our university and programs.',
        to: '#'
      },
      {
        label: 'Undergraduate',
        icon: 'i-lucide-book-open',
        description: 'Undergraduate admission procedures and requirements.',
        to: '#'
      },
      {
        label: 'Graduate',
        icon: 'i-lucide-briefcase',
        description: 'Graduate admission information and research opportunities.',
        to: '#'
      }
    ]
  },
  {
    label: 'Research',
    icon: 'i-lucide-flask-conical',
    description: 'Explore research centers, projects, and publications.',
    to: '#'
  },
  {
    label: 'News',
    icon: 'i-lucide-file-text',
    description: 'Latest news and announcements.',
    to: '#'
  },
  {
    label: 'Downloads',
    icon: 'i-lucide-download-cloud',
    description: 'Download forms, brochures and resources.',
    to: '#'
  }
])
</script>


