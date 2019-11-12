<template>
  <div>
    <!-- <div class="h-48 bg-cover bg-center" :style="{ backgroundImage: `url('${property.imageUrl}')` }"></div> -->
    <div class="relative pb-5/6">
      <img class="absolute h-full w-full object-cover rounded-lg shadow-md" :src="property.imageUrl" :alt="property.imageAlt">
    </div>
    <div class="relative px-4 -mt-16">
      <div class="bg-white p-6 rounded-lg shadow-lg">
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
          <svg v-for="i in 5" :key="i" :class="i <= property.rating ? 'text-teal-500' : 'text-gray-400'" class="h-4 w-4 mr-1 fill-current" viewBox="0 0 576 512" xmlns="http://www.w3.org/2000/svg">
            <path d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z"/>
            <!-- <path d="M12 4.435C10.011-.964 0-.162 0 8.003 0 12.071 3.06 17.484 12 23c8.94-5.516 12-10.929 12-14.997C24-.115 14-.996 12 4.435z"/> -->
          </svg>
          <span class="ml-2 text-gray-600 text-sm">{{ property.reviewCount }} reviews</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['property'],
}
</script>

