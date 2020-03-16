<template>
  <div class="home-container">
    <div class="home">
      <img class="bg-main" src="../assets/img/bg-main2.png">
      <img class="bg-main" src="../assets/img/bg-main1.png">
      <img class="main-person" src="../assets/img/icon.png">
    </div>
    <div class="hello">
      <span>Im Says</span>
      <div>{{ msg }}</div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero, excepturi? Amet mollitia nihil nemo at asperiores, quibusdam quaerat, saepe numquam illum deserunt, suscipit quia accusantium enim odio ullam aperiam doloremque!</p>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
  private msgArr = ['Hello', 'Hay..', 'Hee...', 'Hallo']
  public msg = "Message"

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
      }
    }

    .hello {
      width: 50%;
      margin-top: 6rem;
      font-size: 2rem;

      div {
        font-size: 6rem;
      }

      p{
        margin: 0;
      }
    }
  }
</style>
