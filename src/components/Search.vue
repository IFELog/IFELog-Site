<template>
  <img class="logo" src="../assets/logo.png">
  <div class="searchbox-wrap">
    <div class="search">
  		<div class="search_input ui_search_box">
        <span class="search_sr" :class="{ 'foncuson': isFoucusOnSearch }">
          <input type="text" @focus="onFocusSearchBox">
        </span>
				<div class="suggest_bd" v-show="isShowSearchResult">
          <ul>
            <li>测试内容啊 啊啊啊啊啊</li>
            <li>测试内容啊 啊啊啊啊啊</li>
            <li>测试内容啊 啊啊啊啊啊</li>
            <li>测试内容啊 啊啊啊啊啊</li>
            <li>测试内容啊 啊啊啊啊啊</li>
            <li>测试内容啊 啊啊啊啊啊</li>
          </ul>
				</div>
  		</div>
      <span class="search_btn">
        <input type="submit" value='{{ btnValue }}'>
      </span>
  	</div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      btnValue: 'Log 一下',
      isFoucusOnSearch: false,
      isShowSearchResult: false
    }
  },
  methods: {
    onFocusSearchBox: function (event) {
      this.isFoucusOnSearch = true
    }
  }
}
</script>

<style lang="stylus">
  .logo
    display: block
    width: 180px
    margin: 0 auto

  .searchbox-wrap
    margin: 22px auto 0
    width: 641px
    text-align: left
    z-index: 100

    .search
      .search_input
        display: inline
        position: relative
        float: left
        width: 539px

      .search_sr
        display: inline-block
        width: 538px
        height: 34px
        overflow: hidden
        background: #fff
        vertical-align: top
        border: 1px solid #b6b6b6
        border-right-width: 0
        border-color: #b8b8b8 transparent #b8b8b8 #b8b8b8
        &:hover
          border-color: #999 transparent #999 #999
        &.foncuson
          border-color: #68C243 transparent #68C243 #68C243

        input
          width: 520px
          height: 22px
          font: 16px/18px arial
          line-height: 22px\9
          margin: 6px 0 0 7px
          padding: 0
          background: transparent
          border: 0
          outline: 0
          -webkit-appearance: none

      .search_btn
        width: auto
        height: auto
        border-bottom: 1px solid transparent

        input
          width: 100px
          height: 36px
          color: white
          font-size: 15px
          letter-spacing: 1px
          background: #68C243
          border: 0
          outline: 0
          -webkit-border-radius: 0
          cursor: pointer

      .search_btn:active
        background-position:-100px 0

      .search_btn_hover
        background-position:-100px 0

      .suggest_bd
        position: absolute
        z-index: 1
        width: 538px
        background: #fff
        border: 1px solid #ccc
        margin-top: -1px;
        overflow: hidden
        box-shadow: 1px 1px 3px #ededed
        -webkit-box-shadow: 1px 1px 3px #ededed
        -moz-box-shadow: 1px 1px 3px #ededed
        -o-box-shadow: 1px 1px 3px #ededed
        li
          width: 522px;
          padding: 0 8px;
          position: relative;
          cursor: default;
          text-decoration: none
          color: #383838;
          font: 14px arial;
          line-height: 22px;
          &:hover
            background-color: rgba(104, 194, 67, .2)



</style>
