<template>
  <article :id="`company-${company.id}`" class="my-10">
    <h1 class="text-2xl font-bold my-3">{{ company.name }}</h1>
    <h2 class="text-xl my-2 font-light">{{ company.position }}</h2>
    <p class="italic">{{ company.timeFrame }}</p>
    <p class="mt-4 italic underline">Обязанности и достижения:</p>
    <ul class="company__tasks list-inside">
      <li
        v-for="(task, idx) in company.tasks" :key="`task-${idx}`"
        class="mt-1"
      >
        {{ task }}
      </li>
    </ul>
    <div class="company__skills mt-4">
      <p class="italic underline mb-2">Применяемые навыки:</p>
      <span
        v-for="(skill, idx) in company.skillsUsed" :key="`skill-${idx}`"
        class="company__skill inline-block py-1 px-2 m-1 rounded-lg"
      >
        {{ skill }}
      </span>
    </div>
  </article>
</template>

<script>
export default {
  name: 'Company',
  props: {
    company: { id: Number, name: String, position: String, timeFrame: String, tasks: Array, skillsUsed: Array}
  }
}
</script>

<style>
.company__tasks {
  list-style-type: disc;
}
.company__skill {
  background-color: rgb(0, 131, 92);
}
</style>