<template>
  <header class="header p-3 rounded-t-lg">
    <strong>
      <g-link to="/">{{ $static.metadata.siteName }}</g-link>
    </strong>
    <nav class="nav">
      <button class="theme__toggle" v-if="darkTheme" @click="switchTheme(true)">
        <g-image src="~/assets/icons/moon.svg" />
      </button>
      <button class="theme__toggle" v-else @click="switchTheme(true)">
        <g-image src="~/assets/icons/sun.svg" />
      </button>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data: () => ({
    darkTheme: false
  }),
  methods: {
    switchTheme (isSwitchNeeded) {
      if (isSwitchNeeded) {
        // toggle theme
        this.darkTheme = !this.darkTheme
      
        // save user's preference
        window.localStorage.setItem('data-theme', this.darkTheme)
      }

      // set theme data
      this.darkTheme ? document.documentElement.setAttribute('data-theme', 'dark') : document.documentElement.removeAttribute('data-theme')
    }
  },
  mounted () {
    // check user previous setting for the browser:
    this.darkTheme = window.localStorage.getItem(`data-theme`) === 'dark'

    // set dark theme nonetheless for the evening and night time
    if (!this.darkTheme) {
      let currentTime = new Date().getHours()
      this.darkTheme = currentTime >= 21 || currentTime < 9
    }
    this.switchTheme(false)
  }
}
</script>


<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 40px;
  background-color: rgb(0, 131, 92);
}

.theme__toggle {
  margin-left: 20px;
}

.theme__toggle {
  position: relative;
  top: 5px;
}
</style>