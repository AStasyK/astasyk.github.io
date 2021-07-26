<template>
  <Layout>
    <h1 class="text-xl sm:text-3xl font-bold my-5 text-center">Профессиональные навыки</h1>
    <SkillCategory
      v-for="skillCategory in skills" :key="`category-${skillCategory.id}`"
      :skillCategory="skillCategory" />
  </Layout>
</template>

<script>
import SkillCategory from '~/components/skills/SkillCategory'

export default {
  metaInfo: {
    title: 'Skills'
  },
  components: {SkillCategory},
  data: () => ({
    skills: [
      {
        id: 1,
        name: 'Frontend',
        skills: 'Vue.js / Angular, HTML, CSS / SCSS,\nBootstrap / Bulma / Vuetify / Angular Material / TailwindCSS'
      },
      {
        id: 2,
        name: 'Backend',
        skills: 'Laravel, Django, Ruby, Node.js, SQL (Oracle/MySQL)'
      },
      {
        id: 3,
        name: 'Languages',
        skills: 'Английский – С2, Немецкий – B2, Японский - B1'
      },
      {
        id: 4,
        name: 'Дополнительно',
        skills: 'Хорошие навыки деловой переписки, грамотность,\nвнимание к деталям, высокая концентрация,\nспособность к поиску и исправлению ошибок,\nспособность к напряженной и монотонной работе,\nспособность к обучению, обработке большого количества информации'
      },
    ]
  })
}
</script>

<style>

</style>