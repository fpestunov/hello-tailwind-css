<template>
  <div>
    <img :src="property.imageUrl" :alt="property.imageAlt">
    <h4>{{ property.title }}</h4>
    <div>
      {{ property.beds }} beds &bull; {{ property.baths }} baths
    </div>
    <div>
      {{ property.formattedPrice }} / wk
    </div>
    <div>
      {{ property.rating }}/5 stars (based on {{ property.reviewCount }} reviews)
    </div>
  </div>
</template>

<script>
export default {
  props: ['property'],
}
</script>
