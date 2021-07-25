<template>
  <div id="app">
    <TheHeader />
    <div class="main-container flex flex-wrap md:flex-nowrap">
      <TheSideBar />
        <main class="w-full md:w-8/12 rounded-br-lg h-full py-3 px-8">
          <transition name="fade" appear>
            <router-view></router-view>
          </transition>
        </main>
    </div>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
    siteDescription
  }
}
</static-query>

<script>
import TheHeader from '~/components/TheHeader'
import TheSideBar from '~/components/TheSidebar'

export default {
  metaInfo() {
    return {
      title: this.$static.metadata.siteName,
      meta: [
        {
          key: 'description',
          name: 'description',
          content: this.$static.metadata.siteDescription
        }
      ]
    }
  },
  components: {TheHeader, TheSideBar}
}
</script>

<style>
:root {
  --color-bg: white;
  --color-text: #111415;
}
[data-theme="dark"] {
  --color-bg: #111115;
  --color-text: #efe8ee;
}
html {
  min-height: 100%;
}
body {
  color: var(--color-text);
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  min-height: 100%;
  margin:0;
  padding:30px;
  line-height: 1.5;
  position: relative;
  background: linear-gradient(to bottom left, hsl(270, 80%, 60%), hsl(300, 80%, 60%), hsl(310, 50%, 80%));
}


#app {
  max-width: 960px;
  margin: 0 auto;
  border-radius: .5em;
  background-color: var(--color-bg);
  /*height: 100%;*/
}
.fade-enter-active {
  transition: opacity .5s;
}

.fade-enter {
  opacity: 0;
}

</style>
