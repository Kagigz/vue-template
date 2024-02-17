<script setup lang="ts">
import settings from '../setup/settings.json'

useHead({
  templateParams: {
    site: {
      name: settings.app_name,
    },
    separator: settings.page_title_separator,
  },
  titleTemplate: settings.page_title ? '%site.name %separator %s' : '%site.name',
  meta: [
    { name: 'description', content: settings.description },
  ],
})
</script>

<template>
  <main>
    <RouterView />
  </main>
</template>
