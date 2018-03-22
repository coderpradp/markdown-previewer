<template>
  <div id="app">
    <app-header></app-header>
    <app-footer></app-footer>
  </div>
</template>

<script>
import Header from './Header'
import Footer from './Footer'

export default {
  name: 'app',
  data() {
    return {}
  },
  components: {
    'app-header': Header,
    'app-footer': Footer
  }
}
</script>

<style>

</style>
