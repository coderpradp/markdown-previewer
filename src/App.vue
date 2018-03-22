<template>
  <div id="container">
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
  height: 100%;
}
h1,
h2,
h3,
h4,
h5 {
  margin: 0;
  padding: 0;
}
body {
  font-family: 'Open Sans', sans-serif;
}
a {
  text-decoration: none;
}
#container {
  min-height: 100%;
  position: relative;
}
</style>
