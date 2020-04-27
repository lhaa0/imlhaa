<template>
  <div class="home-container">
    <div class="home">
      <img class="bg-main second" src="../assets/img/bg-main2.png">
      <img class="bg-main first" src="../assets/img/bg-main1.png">
      <img class="main-person" src="../assets/img/icon.png">
    </div>
    <div class="hello">
      <span>Im Says</span>
      <div>{{ checkMessage() }}</div>
      <p>Join My Discord Server!</p>
      <iframe src="https://discordapp.com/widget?id=695980892291858443&theme=dark&username=lhaa" width="350" height="500" allowtransparency="true" frameborder="0"></iframe>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
  private msgArr = ['Hello', 'Hay..', 'Hee...', 'Hallo']
  public msg = "Message"

  i = 0;
  checkMessage(){
    this.msg = this.msgArr[this.i]
    return this.msg
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .home-container {
    display: flex;
    justify-content: space-between;
    margin: 24px;

    .home {
      width: 80%;

      img{
        position: absolute;
      }
      img.main-person {
        left: 25%;
        width: 36%;
        transform: translate(-25%);
      }
      img.bg-main{
        width: 56%;

        &.first {
          animation: bg-main1 7s
          ease-out
          0s
          alternate
          infinite
          none
          running;
        }
        &.second {
          animation: bg-main1 7s
          ease-out
          0s
          alternate-reverse
          infinite
          none
          running;
        }
      }
    }

    .hello {
      width: 50%;
      margin-top: 2rem;
      font-size: 2rem;

      div {
        font-size: 6rem;
      }

      p{
        margin: 0;
      }

      iframe {
        margin-top : 1rem;
        width: 100%;
      }
    }
  }

  @keyframes bg-main1 {
          25%{
            transform: rotate(10deg);
          }
          50%{
            transform: rotate(20deg);
          }
          75%{
            transform: rotate(10deg);
          }
          100%{
            transform: rotate(0deg);
          }
        }
</style>