<template>
  <div class="mx-4 shadow-lg max-h-[24rem] bg-white grid grid-cols-1 grid-rows-2 rounded-md">
    <!-- Image -->
    <div class="rounded-t-md md:rounded-tr-none">
      <img :src="country.flag" alt="" class="w-full h-48 object-cover" />
    </div>

    <!-- Country details -->
    <div class="px-6 pt-6 pb-12">
      <h3 class="font-[800] text-lg mb-4">{{ country.name }}</h3>

      <p class="font-[600]">
        Population: <span class="font-[300]">{{ country.population }}</span>
      </p>
      <p class="font-[600]">
        Region: <span class="font-[300]">{{ country.region }}</span>
      </p>
      <p class="font-[600]">
        Capital: <span class="font-[300]">{{ country.capital }}</span>
      </p>
    </div>
  </div>
</template>

<script setup>
defineProps({
  country: {
    required: true,
    type: Object
  }
})
</script>
