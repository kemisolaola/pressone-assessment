<template>
  <nav class="nav-bar">
    <div class="nav-items">
      <div class="logo">
        <img src="../assets/logo.svg" alt="Logo" class="logo-img" />
      </div>
      <div class="nav-links">
        <a :href="link.id" v-for="(link, index) in navLinks" :key="index">
          <button class="nav-btn">{{ link.name }}</button>
        </a>
        
      </div>
      <div class="get-pressone">
        <button class="outline-btn">Get PressOne</button>
      </div>
      <div class="mobile-icon" @click="toggleSidebar">
        <img src="../assets//more.png" alt="" />
      </div>
    </div>
  </nav>

  <div class="sidebar" :class="{ open: isSidebarOpen }">
    <ul>
      <li v-for="(link, index) in navLinks" :key="index">
        <a :href="link.id" >
        <button class="nav-btn white-text">{{ link.name }}</button>
        </a>
      </li>
      <li><button class="nav-btn white-text">Get PressOne</button></li>
    </ul>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const navLinks = ref([
    {name:"About Us", id: '#aboutus'},
    {name:"Pricing", id: '#pricing'},
    {name:"Product", id: '#product'},
    {name:"Support", id: '#support'},
  ])
    const isSidebarOpen = ref(false);
    const toggleSidebar = () => {
      isSidebarOpen.value = !isSidebarOpen.value;
    };
    return {
      navLinks,
      toggleSidebar,
      isSidebarOpen,
    };
  },
};
</script>
<style scoped></style>
