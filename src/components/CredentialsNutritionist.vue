<template>
  <div class="div-header-bar " :class="{'scroll': scrollScreenHeader == true}">
    <div class="div-img-logo">
      <img src="../assets/img/logo.png" />
    </div>
    <div class="div-name-nutri">
      <h1>Samuel Rodrigues</h1>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  props: {
    scrollScreenHeader: Boolean,
  },
});
</script>

<style lang="scss">
.div-header-bar {
  height: 100px;



  &.scroll {
    
  }
}

.div-name-nutri {
  margin: 5px auto;
  display: block;

  h1 {
    font-size: 22px;
    margin: 0;
    margin-left: 0px;
    display: block;
    font-family: "Quicksand", sans-serif;
    color: #29a044;
  }
}

.div-img-logo {
  height: 71px;
  width: 93px;
  margin: 0 auto;
  margin-top: 30px;

  & img {
    width: 100%;
    height: 100%;
    margin-left: 9px;
  }
}
</style>