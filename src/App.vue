<template>
  <div>
    <!-- 공통 이벤트 영역 -->
    <CommonEventComponent />
    
    <!-- header 영역 -->
    <HeaderComponent />
   
    <!-- about me 영역 -->
    <AboutComponent />

    <!-- projects 영역 -->
    <ProjectComponent />

    <!-- footer -->
    <FooterComponent />
  </div>
</template>

<script>
export default {
  name: 'App',
}
</script>

<script setup>
import CommonEventComponent from './components/CommonEventComponent.vue'
import HeaderComponent from './components/HeaderComponent.vue'
import AboutComponent from './components/AboutComponent.vue'
import ProjectComponent from './components/ProjectComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
</script>

<style>

</style>
