<template>
  <article :id="`skillcategory-${skillCategory.id}`" class="skill__category my-10">
    <h1 class="text-lg sm:text-2xl font-bold my-3">{{ skillCategory.name }}</h1>
    <div class="text-sm sm:text-base pl-1 sm:pl-3 relative left-4 sm:left-7 border-l-4 whitespace-pre-line">{{ skillCategory.skills }}</div>
  </article>
</template>

<script>
export default {
  name: 'SkillCategory',
  props: {
    skillCategory: { id: Number, name: String, skills: String, showMode: String }
  }
}
</script>

<style>
.skill__category div {
  border-color: rgb(0, 131, 92);
}
</style>