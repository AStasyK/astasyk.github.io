<template>
  <article :id="`uni-${uni.id}`" class="px-2 sm:px-0 mb-10">
    <h1 class="text-xl sm:text-2xl font-bold my-3">{{ uni.name }}</h1>
    <p class="italic">{{ uni.timeFrame }}</p>
    <h2 class="text-lg sm:text-xl mt-2 font-light">{{ uni.degree }}</h2>
    <h2 class="text-base sm:text-lg font-light">{{ uni.degreeDetails }}</h2>
    <p class="mt-4 italic underline">ВКР: {{ uni.thesis }}</p>
  </article>
</template>

<script>
export default {
  name: 'University',
  props: {
    uni: { id: Number, name: String, timeFrame: String, degree: String, degreeDetails: String, thesis: Array }
  }
}
</script>

<style>
</style>