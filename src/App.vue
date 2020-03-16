<template>
  <div id="app">
    <div id="nav">
      <div class="nav-title">
        <div class="title">i'm<label>Lhaa.</label></div>
      </div>
      <div class="nav-group">
        <div>
          <router-link to="/">Home</router-link>
        </div>
        <div>
          <router-link to="/about">Profile</router-link>
        </div>
      </div>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
@import "assets/style/font.scss";
@import "assets/style/app.scss";
</style>
