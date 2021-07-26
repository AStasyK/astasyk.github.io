<template>
  <Layout>
    <h1 class="text-xl sm:text-3xl font-bold my-5 text-center">Опыт работы</h1>
    <Company v-for="company in experience" :key="`company-${company.id}`" :company="company" />
  </Layout>
</template>

<script>
import Company from '~/components/experience/Company.vue'

export default {
  metaInfo: {
    title: 'Working experience'
  },
  components: {Company},
  data: () => ({
    experience: [
      {
        id: 1,
        name: 'Персональные проекты',
        position: 'Fullstack web-developer',
        timeFrame: 'Январь 2019 — По наст. время',
        tasks: [
          'Разработка MVP проекта на Vue.js (Vuex, Vue router)',
          'Разработка интерфейсов на Angular, React',
          'Разработка бэкэндов на Laravel, Django, Express.js',
          'Разработка бэкэндов на Laravel, Django, Express.js',
          'Продумывание архитектуры приложений',
          'Разработка интерфейсов как SPA + API, так и в стиле HTML over the Wire + микрофронтенды',
          'Учебный Space Shooter на Unity'
        ],
        skillsUsed: ['Vue.js', 'Bulma', 'Laravel', 'Django', 'Базы данных', 'Angular', 'Node.js', 'TailwindCSS', 'C#']
      },
      {
        id: 2,
        name: 'T-Systems Rus',
        position: 'Software Engineer',
        timeFrame: 'Июль 2017 — Сентябрь 2019',
        tasks: [
          'Планирование и разработка интерфейса сервиса для немецкой стороны: Angular, material design',
          'Работа с JWT авторизацией',
          'Написание комплексных SQL запросов. Работа с Oracle СУБД',
          'Back-end разработка API: Spring Boot, Ruby on Rails',
          'Еженедельные коммуникации с немецкими коллегами по процессу разработки',
          'Ведение задач в JIRA по спринтам',
          'Разработка интерфейса сервиса для записи сотрудников компании на плановые медосмотры: Vue.js, Vuetify',
          'Написание автоматических тестов: Rspec + Watir',
          'Участие во VueSchool в качестве ментора'
        ],
        skillsUsed: ['Angular', 'Typescript', 'Spring Boot', 'Oracle', 'Vue.js', 'Ruby on Rails', 'Ruby']
      },
      {
        id: 3,
        name: 'ООО "Ниссан Мэнуфэкчуринг РУС"',
        position: 'Специалист налогового отдела',
        timeFrame: 'Сентябрь 2014 — Март 2017',
        tasks: [
          'Ведение налогового учёта по НДС',
          'Сдача налоговой декларации по НДС',
          'Квартальное закрытие НДС счетов, заведение необходимых проводок в SAP',
          'Сбор документов и ответы по встречным налоговым проверкам',
          'Написание документации по зонам ответственности',
          'Обработка большого количества данных в MS Excel и SAP, коммуникации с коллегами по ошибкам в налоговом учёте',
          'Отслеживание последних изменений в законодательстве по налоговому учёту',
          'Написание VBA-скриптов'
        ],
        skillsUsed: ['MS Excel', 'MS Word', 'SAP']
      }
      
    ]
  })
}
</script>

<style>

</style>