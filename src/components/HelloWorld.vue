<template>
  <div class="home-container">
    <div class="home">
      <div>
        <img class="bg-main second" src="../assets/img/bg-main2.png">
        <img class="bg-main first" src="../assets/img/bg-main1.png">
        <img class="main-person" src="../assets/img/icon.png">
      </div>
    </div>
    <div class="hello">
      <div class="discord-widget">
        <span>Im Says</span>
        <div>{{ checkMessage() }}</div>
        <!-- <p>Join My Discord Server!</p>
        <iframe src="https://discordapp.com/widget?id=695980892291858443&theme=dark" allowtransparency="true" frameborder="0"></iframe> -->
      </div>
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
      margin-top: 0vh;
      font-size: 2rem;

      p{
        margin: 0;
      }

      div.discord-widget {
        width: 100%;
        height: 50vh;
        
        div {
          font-size: 6rem;
        }
        iframe{
          height: 50vh;
          width: 38%;
          margin: 0 auto;
          position: absolute;
          bottom: 1vh;
          right: 1vh;
        }
      }
    }
  }

   @media (max-width: 920px) {
    .home-container{
      display: unset;
      justify-content: unset;
      margin: unset;

      .home {
        height: 45vh;
        margin: auto;
        position: relative;

        img{
          width: 100% !important;
        }
      }

      .hello {
        width: 80%;
        margin: auto;
      }

      @media only screen 
      and (min-device-width : 768px) 
      and (max-device-width : 1024px) 
      and (orientation : portrait) { 
        .home {
          height: 65vh;
        }
      }

      @media only screen 
      and (min-device-width : 375px) 
      and (max-device-width : 812px) 
      and (-webkit-device-pixel-ratio : 3)
      and (orientation : landscape) { 
        .home {
          height: 145vh !important;
        }
      }

      @media (orientation: landscape) {
        .home {
          height: 125vh;
          width: 65%;
        }
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