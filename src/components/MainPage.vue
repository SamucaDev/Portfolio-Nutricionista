<template>
  <div class="div-header-bar">
    <CredentialsNutritionist :scrollScreenHeader="scrollScreenHeader" />
    <div
      class="menu-option-function"
      :class="{ scrollCHeck: scrollScreenHeader == true }"
    >
      <div id="option-menu">
        <span class="button-option-menu select">Home</span>
        <span class="button-option-menu">Fale com o Nutri</span>
        <span class="button-option-menu">Sobre o Samuca</span>
        <span class="button-option-menu">Venha pro instagram</span>
      </div>
    </div>
    <SliderImages :scrollScreenHeader="scrollScreenHeader" />

    <ApresentationNutri />
    <sectionInformationNutri />

    
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import CredentialsNutritionist from "../components/CredentialsNutritionist.vue";
import SliderImages from "../components/SliderImages.vue";
import ApresentationNutri from "../components/ApresentationNutri.vue";
import sectionInformationNutri from "../components/sectionInformationNutri.vue";

export default Vue.extend({
  data() {
    return {
      scrollScreenHeader: false,
    };
  },
  components: {
    CredentialsNutritionist,
    SliderImages,
    ApresentationNutri,
    sectionInformationNutri
  },

  methods: {
    handleScroll() {
      console.log(window.pageYOffset);
      if (window.pageYOffset >= 140) {
        this.scrollScreenHeader = true;
      } else {
        this.scrollScreenHeader = false;
      }

      console.log(this.scrollScreenHeader);
    },
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  },
});
</script>
s
<style lang="scss">
.menu-option-function {
  background: #fff;
  margin-top: 9px;

  &.scrollCHeck {
    position: fixed;
    z-index: 3;
    margin-top: 0;
    margin: 0 auto;
    top: 0;
    transition: position 3s;
    width: 100%;
  }
}

#option-menu {
  display: flex;
  align-content: space-around;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.button-option-menu {
  margin: 21px 35px;
  color: #000;
  border: none;
  font-size: 20px;
  font-weight: 600;
  font-family: "Quicksand", sans-serif;
  padding: 10px 15px;
  cursor: pointer;
  &.select {
    background: #99ce54;
  }
}
</style>