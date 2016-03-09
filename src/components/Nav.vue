<template>
  <header>
    <ul class="nav-list">
      <li v-for="item in items">
        <a href='{{ item.url }}'>{{ item.nav }}</a>
      </li>
    </ul>
  </header>
</template>

<script>
export default {
  data () {
    return {
      items: [
        { nav: 'Home', url: 'aaa' },
        { nav: 'About', url: 'aaa' },
        { nav: 'GitHub', url: 'aaa' },
        { nav: 'Content', url: 'aaa' }
      ]
    }
  }
}
</script>

<style lang="stylus">
  header
    width: 100%
    position: fixed
    top: 0
    right: 0
    font-size: 1.0em
    padding: 0px 20px
    ul
      float: right
    li
      float: left
      margin-left: 0.2em
      padding: 10px 12px
      a
        color: #383838
        &:hover
          color: #000000


</style>
