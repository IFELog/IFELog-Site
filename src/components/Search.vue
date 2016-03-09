<template>
  <img class="logo" src="https://www.baidu.com/img/bd_logo1.png">
  <div class="searchbox-wrap">
    <div class="search">
  		<div class="search_input ui_search_box">
        <span class="search_sr" >
          <input type="text" id="search_text">
        </span>
				<div class="suggest_nc" id="search_result">
					<!-- <a href="javascript:">测试内容啊 啊啊啊啊啊</a> -->
				</div>
  		</div>
      <span class="search_btn">
        <input type="submit" value='{{ btnValue }}' id="submit_btn">
      </span>
  	</div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      btnValue: 'Log 一下'
    }
  }
}
</script>

<style lang="stylus">
  .logo
    display: block
    width: 270px
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
        border-color: #b8b8b8 transparent #ccc #b8b8b8
        &:hover
          border-color: #999 transparent #b3b3b3 #999
          /*     border-color: #4791ff transparent #4791ff #4791ff */

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
          background: #3385ff
          border: 0
          outline: 0
          -webkit-border-radius: 0
          cursor: pointer

      .search_btn:active
        background-position:-100px 0

      .search_btn_hover
        background-position:-100px 0

      .suggest_bd
        display: none
        position: absolute
        width: 100%
        left: -1px
        background: white
        top: 30px
        border: 1px solid #999

</style>
