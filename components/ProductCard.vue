<template>
  <div>
    <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
      <NuxtLink :to="`/products/${product?.id}`">
        <div class="relative flex items-center justify-center w-full h-80">
          <img class="absolute h-full" :src="product?.image" :alt="product?.title" />
        </div>
      </NuxtLink>
      <div class="p-5">
        <NuxtLink :to="`/products/${product?.id}`">
          <h5 class="h-16 mb-2 overflow-hidden text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
            {{ product?.title }}
          </h5>
        </NuxtLink>
        <p class="h-12 mb-3 overflow-hidden font-normal text-gray-700 dark:text-gray-400">
          {{ product?.description }}
        </p>
        <h1 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
          ${{ product?.price }}
        </h1>
        <NuxtLink :to="`/products/${product?.id}`"
          class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
          Read more
          <svg aria-hidden="true" class="w-4 h-4 ml-2 -mr-1" fill="currentColor" viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg">
            <path fill-rule="evenodd"
              d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z"
              clip-rule="evenodd"></path>
          </svg>
        </NuxtLink>
      </div>
    </div>

  </div>
</template>

<script setup>
const { product } = defineProps(['product'])
</script>

<style lang="scss" scoped>

</style>