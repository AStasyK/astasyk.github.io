<template>
  <Layout>
    <h1 class="text-xl sm:text-3xl font-bold my-5 text-center">Высшее образование</h1>
    <University v-for="university in education" :key="`uni-${university.id}`" :uni="university" />
  </Layout>
</template>

<script>
import University from '~/components/education/University.vue'

export default {
  metaInfo: {
    title: 'Education'
  },
  components: {University},
  data: () => ({
    education: [
      {
        id: 1,
        name: 'Санкт-Петербургский политехнический университет Петра Великого',
        degree: 'Магистр по направлению “Прикладная информатика”',
        degreeDetails: 'Программа “Технологии веб-разработки”',
        timeFrame: 'Сентябрь 2015 — Январь 2018',
        thesis: 'Методика анализа тональности русскоязычных текстов (с применением машинного обучения на языке Ruby)'
      },
      {
        id: 2,
        name: 'Высшая школа менеджмента СПбГУ',
        degree: 'Бакалавр по направлению “Менеджмент”',
        degreeDetails: 'Профиль “Финансовый менеджмент”',
        timeFrame: 'Сентябрь 2010 — Июнь 2014',
        thesis: 'Управление стоимостью компании "Верофарм."'
      }
    ]
  })
}
</script>

<style>

</style>