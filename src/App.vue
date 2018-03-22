<template>
  <div>
    <app-header></app-header>
    <app-markdown></app-markdown>
    <app-footer></app-footer>
  </div>
</template>

<script>
import Header from './Header'
import Markdown from './Markdown'
import Footer from './Footer'

export default {
  name: 'app',
  components: {
    'app-markdown': Markdown,
    'app-header': Header,
    'app-footer': Footer
  }
}
</script>

<style>
html,
body {
  margin: 0;
  padding: 0;
  font-family: 'Open Sans', sans-serif;
}
a {
  text-decoration: none;
}
</style>
