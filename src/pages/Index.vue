<template>
  <Layout>
    <article class="p-1 sms:p-3">
      <header>
        <h1 class="text-lg font-bold mt-2 mb-5 sm:text-2xl text-center md:mb-10">Добро пожаловать на сайт!</h1>
      </header>
      <div>
        <p class="index__paragraph text-sm md:text-base">Меня зовут Кучурина Анастасия. Я программист/fullstack веб-разработчик из Санкт-Петербурга.</p>
        <p class="index__paragraph text-sm md:text-base">Мне нравится решать сложные задачи, и в программировании никогда без таковых не останешься. Поэтому мне очень нравится эта профессия.</p>
        <p class="index__paragraph text-sm md:text-base">Я люблю разбираться в вещах и узнавать новое, осваивать разные области знаний. Поэтому как программисту мне нравится работать как над веб-интерфейсами, так и с бэкэндом, и с базами данных. Понимать, как работает вся система, позволяет лучше проникнуться делом.</p>
        <p class="index__paragraph text-sm md:text-base">Мне также нравится изучать иностранные языки и иметь возможность понимать людей разных стран. Я использую английский на повседневной основе, на немецком хорошо пишу и могу понимать японский. Также по верхам знаю ещё пару европейских языков.</p>
        <p class="index__paragraph text-sm md:text-base">Обладаю предрасположенностью к нахождению ошибок и их исправлению. В своей жизни абсолютно в разных областях мне часто доводится находить несоответствия, ошибки, баги и работать над улучшением ситуации.</p>
      </div>
    </article>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Greetings'
  }
}
</script>

<style>
.index__paragraph {
  margin-bottom: 15px;
  text-align: justify;
}
</style>
