<template>
  <div id="app">
    <navlist></navlist>
    <div class="container">
      <search></search>
    </div>
  </div>
</template>

<script>
import Navlist from './components/Nav'
import Search from './components/Search'

export default {
  components: {
    Navlist, Search
  }
}
</script>

<style lang="stylus">
  *
    margin: 0
    padding: 0

  ul, li
    list-style: none

  html
    height: 100%
    transform: scale(1)

  body
    height: 100%
    padding-top: 38px
    overflow: hidden

  #app
    font-family: Helvetica, sans-serif


  .container
    margin-top: 140px
    /*display: flex
    align-items: center
    justify-content: center*/

</style>
