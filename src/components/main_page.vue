<template>
  <div class="main">
    <header id="header">
      <div class="button-area">
        <p>
          알림
        </p>
        <p>
          메시지
        </p>
      </div>
    </header>

    <nav id="nav" class="nav">
      <div class="nav-title">
        <p>DOTORI NAMU</p>
      </div>
      <ul class="nav-list">
        <li>캘린더</li>
        <li>회원</li>
        <li>CS</li>
        <li>센터관리</li>
        <li>분석</li>
      </ul>
    </nav>
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
  #header{
    display:flex;
    justify-content: flex-end;
    align-items: center;
    width:100vw;
    height:60px;
    border-bottom:1px solid #eee;
    & .button-area{
      display:flex;
      padding-right:30px;

      & p{
        padding-right:30px;
        font-size:14px;
        font-style:italic;
        color:#333;
      }
    }
  }

  #nav{
    margin:0;
    padding:0;
    position:relative;
    left:0;
    top:-60px;
    z-index:1;
    width:150px;
    height:100vh;
    text-align:center;
    border-right:1px solid #eee;
    background-color:#fff;
    & p{
      border-bottom:1px solid #eee;
      padding-top:10px;
      padding-bottom:14px;
    }
    & ul{
      list-style-type: none;
      text-align: center;
      & li{
        margin-bottom:15px;
        text-align: left;
      }
    }
  }
</style>
