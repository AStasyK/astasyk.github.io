<template>
  <aside class="w-full md:w-4/12 md:rounded-bl-lg">
    <!-- identity -->
    <div id="identity" class="text-center py-3">
      <g-image id="identity-photo" class="rounded-full border-2 my-1 mx-auto" src="~/assets/img/photo.jpg" width="150" quality="100" />
      <h2 id="identity-name" class="text-white text-xl mt-5">Анастасия Кучурина</h2>
    </div>
    <!-- links -->
    <div id="page-links" class="flex flex-wrap justify-center md:block mt-5 mb-3 text-center px-5">
      <g-link
        v-for="(link, idx) in links" :key="idx"
        class="nav__link rounded-lg text-center block mx-2 py-1 px-2 sm:p-3 md:mx-0 mb-2 md:mb-5"
        :to="link.address"
      >
        {{link.name}}
      </g-link>
    </div>
    <!-- contacts -->
    <div id="contacts" class="p-3 text-center">
      <h3 class="text-white">Контакты: 
        <g-link to="https://career.habr.com/kuchurinaaa" class="contact__link font-bold">Хабр Карьера</g-link>
      </h3>
    </div>
    <div id="copyright" class="text-center text-white my-2">{{new Date().getFullYear()}}. &copy; Анастасия Кучурина</div>
  </aside>
</template>

<script>
export default {
  data: () => ({
    links: [
      { address: '/', name: 'На главную' },
      { address: '/skills/', name: 'Профессиональные навыки' },
      { address: '/experience/', name: 'Опыт' },
      { address: '/education/', name: 'Образование' },
      { address: '/about/', name: 'О себе' }
    ]
  })
}
</script>

<style>
aside {
  background-color: hsl(258, 63%, 51%);
}
.nav__link {
  background-color: var(--color-bg);
}
.contact__link {
  color: rgb(0, 131, 92);
}
</style>