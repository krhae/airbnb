<template lang="pug">
  .div.main-view
    navigation-bar(v-if="showNavBar")
</template>

<script>
import NavigationBar from './NavigationBar'

export default {
  name: 'MainView',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      showNavBar: true
    }
  },
  components: {
    NavigationBar
    // TODO: handle action btn click and switch out main element
  }
}
</script>

<style lang="scss" scoped>

</style>
