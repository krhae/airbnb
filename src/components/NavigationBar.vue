<template lang="pug">
  div.nav-bar(v-if="showNavBar")
      .logo KH
      nav.nav-bar-container
        ul.nav-bar-item(v-for="bar in navigationBars")
          li(v-on:click="handleNavBarItemClick(bar)") {{ bar }}
</template>

<script>
export default {
  name: 'NavigationBar',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      navigationBars: ['Welcome', 'Rules', 'Transportation & Parking', 'The apartment', 'Seattle'],
      showNavBar: true
    }
  },
  methods: {
    handleNavBarItemClick (navBarItem) {
      alert(navBarItem)

      // TODO: emit action
    }
  }
}
</script>

<style lang="scss" scoped>
.nav-bar {
  width: 100vw;
  height: 50px;

  .logo {
    font-family: "Montserrat", sans-serif;
    font-size: 18px;
    display: inline-block;
    float: left;
  }

  nav {
    float: left;
    font-family: "Montserrat", sans-serif;
    font-size: 9px;
    display: inline-block;

    ul {
      list-style: none;
      overflow: hidden;
      text-align: right;
      float: left;
      padding: 15px;

      li {
        display: inline-block;
        margin-left: 0px;
        line-height: 1.5;
        cursor: pointer;
        cursor: hand;
      }
    }
  }
}
</style>
