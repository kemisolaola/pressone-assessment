<template>
  <HeaderView/>
  <HomePage/>
  <FooterView/>
</template>

<script>
import HeaderView from './components/HeaderView.vue'
import HomePage from './components/HomePage.vue';
import FooterView from './components/FooterView.vue';

export default {
  components: {
    HeaderView,
    HomePage,
    FooterView
},
  setup() {

    return {
    };
  },
};
</script>
<style>
</style>
