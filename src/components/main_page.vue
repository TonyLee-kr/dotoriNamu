<template>
  <div class="main">

    <header id="header">
      <h1 class="logo-area">
        <img src="" alt="도토리 나무"/>
        <span class="main-title">DOTORI NAMU</span>
      </h1>

      <ul class="manu-list">
        <li>
          <img src="" alt=""/>
          <h2 class="list-title">캘린더</h2>
        </li>
        <li>
          <img src="" alt=""/>
          <h2 class="list-title">회원</h2>
        </li>
        <li>
          <img src="" alt=""/>
          <h2 class="list-title">CS</h2>
        </li>
        <li>
          <img src="" alt=""/>
          <h2 class="list-title">센터관리</h2>
        </li>
        <li>
          <img src="" alt=""/>
          <h2 class="list-title">분석</h2>
        </li>
      </ul>

      <div class="button-area">
        <p>
          알림
        </p>
        <p>
          메시지
        </p>
      </div>
    </header>

  </div>

  <div id="contents" class="contents">

  </div>

</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component'

@Options({
  props: {
    msg: String
  }
})
export default class mainPage extends Vue {
  msg!: string
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import './../assets/style/reset.css';
  // *{
  //   margin:0;
  //   padding:0;
  // }
  // html, body, ul, li, p, div, header, footer, section{
  //   margin:0;
  //   padding:0;
  // }

  #header{
    display:flex;
    justify-content: space-between;
    align-items: center;
    width:100vw;
    height:60px;
    border-bottom:1px solid #eee;

    & .logo-area {
      padding-left:30px;
      font-size:18px;
    }

    & .manu-list{
      list-style-type: none;
      display:flex;
      align-items: center;
      justify-content: flex-start;

      & li{
        display:flex;
        padding-right: 40px;

        & .list-title{
          font-size:14px;
        }

      }
    }
    & .button-area{
      display:flex;
      padding-right:60px;

      & p{
        padding-right:30px;
        font-size:14px;
        font-style:italic;
        color:#333;
      }
    }
  }

  #contents{
    width:100vw;
    height:100vh;
    background-color:#efefef;
  }
</style>
