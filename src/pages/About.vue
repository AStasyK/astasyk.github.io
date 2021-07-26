<template>
  <Layout>
    <h1 class="text-xl sm:text-3xl font-bold my-5 text-center">О себе</h1>
    <p class="px-1 text-sm md:text-base text-light text-justify leading-relaxed">
      Fullstack веб-разработчик с ориентацией на фронтенд и углублённым понимаем Vue.js и Angular.
      Имею отдельный интерес к написанию сложных SQL запросов.<br><br>
      Обладаю развитым вниманием к деталям, высокой концентрацией, ответственностью и способностью к обучению.
      С готовностью разбираюсь в необходимых для работы технологиях.
      Люблю копать глубже в разных предметных областях и решать комплексные задачи.<br><br>
      Английский - мой второй язык во всех сферах жизни.
      Есть письменный немецкий. Также понимаю по-японски.

    <h2 class="px-1 text-xl my-4">Личные интересы</h2>
    <div id="interests" class="px-1">
      <span
        v-for="(interest, idx) in interests.split(', ')" :key="`interest-${idx}`"
        class="company__skill inline-block text-sm sm:text-base py-1 px-2 m-1 rounded-lg"
      >{{ interest.toLowerCase() }}</span>
      <span
        class="inline-block text-sm sm:text-base p-1 m-1"
      >и другие...</span>
    </div>

  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'About me'
  },
  data: () => ({
    interests: 'Иностранные языки, программирование, чтение, игры на консоли, игра на музыкальных инструментах, пение, психология и физиология, история, природа'
  })
}
</script>
