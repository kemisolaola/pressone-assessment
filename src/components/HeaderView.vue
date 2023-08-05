<template>
  <nav class="nav-bar">
    <div class="nav-items">
      <div class="logo">
        <img src="../assets/logo.svg" alt="Logo" class="logo-img" />
      </div>
      <div class="nav-links">
        <button v-for="(button, index) in buttons" :key="index" class="nav-btn">{{ button }}</button>
      </div>
      <div class="get-pressone">
        <button class="outline-btn">
        Get PressOne
      </button>
      </div>     
    </div>
  </nav>
</template>

<script>

import { ref } from 'vue';
export default {
  setup() {
  const  buttons = ref(['About Us', 'Pricing', 'Product', 'Support'])
return {
  buttons
};
},
};
</script>

