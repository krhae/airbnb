<template lang="pug">
  .div.main-view
    navigation-bar(v-if="showNavBar")
    help-form
</template>

<script>
import NavigationBar from './NavigationBar'
import HelpForm from './HelpForm'

export default {
  name: 'MainView',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      showNavBar: true
    }
  },
  components: {
    NavigationBar,
    HelpForm
    // TODO: handle action btn click and switch out main element
  }
}
</script>

<style lang="scss" scoped>

</style>
