<template>
  <div class="bg-white rounded-lg overflow-hidden">
    <img :src="property.imageUrl" :alt="property.imageAlt">
    <div class="p-6">
      <div class="flex items-baseline">
        <span class="bg-teal-500 text-white text-xs px-2 inline-block rounded-full uppercase font-semibold tracking-wide">New</span>
        <div class="ml-2 text-gray-600 text-xs uppercase font-semibold tracking-wide">
          {{ property.beds }} beds &bull; {{ property.baths }} baths
        </div>
      </div>
      <h4 class="mt-1 font-semibold text-lg leading-tight truncate">{{ property.title }}</h4>
      <div class="mt-1">
        {{ property.formattedPrice }} <span class="text-gray-600 text-sm">/ wk</span>
      </div>
      <div class="mt-2 flex items-center">
        <svg v-for="i in 5" :key="i" :class="i <= property.rating ? 'text-teal-500' : 'text-gray-400'" class="h-4 w-4 mr-1 fill-current" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path d="M12 4.435C10.011-.964 0-.162 0 8.003 0 12.071 3.06 17.484 12 23c8.94-5.516 12-10.929 12-14.997C24-.115 14-.996 12 4.435z"/>
        </svg>
        <span class="ml-2 text-gray-600 text-sm">{{ property.reviewCount }} reviews</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['property'],
}
</script>

