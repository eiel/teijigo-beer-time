<template>
  <div id="main-container" :class="$style.mainContainer">
    <tbt-top-link>
      <tbt-logo />
    </tbt-top-link>
    <slot />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';
import TbtTopLink from '@/components/atoms/TbtTopLink.vue';
import TbtLogo from '@/components/atoms/TbtLogo.vue';

@Component({
  components: {
    TbtTopLink,
    TbtLogo,
  },
})
export default class TbtMenu extends Vue {}
</script>

<style module>
.mainContainer {
  width: 80%;
  margin-left: 20%;
  border-left: 5px solid gainsboro;
  padding-top: 60px;
  text-align: center;
}

@media screen and (max-width: 900px) {
  .mainContainer {
    width: 100%;
    padding-top: 20px;
    margin: 0;
    border-top: 1px solid black;
    border-left: none;
  }
}
</style>
