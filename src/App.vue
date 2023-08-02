<template>
  <div>
    <!-- 공통 이벤트 영역 -->
    <common-event-component />
    
    <!-- header 영역 -->
    <header-component />
   
    <!-- about me 영역 -->
    <about-component />

    <!-- projects 영역 -->
    <project-component />

    <!-- career 영역 -->
    <career-component />

    <!-- skills 영역 -->
    <skill-component />

    <!-- footer -->
    <footer-component />

    <!--  -->
  </div>
</template>

<script>
export default {
  name: 'App',
}
</script>

<script setup>
import CommonEventComponent from './components/commonEvent-component.vue'
import HeaderComponent from './components/header-component.vue'
import AboutComponent from './components/about-component.vue'
import CareerComponent from './components/career-component.vue'
import ProjectComponent from './components/project-component.vue'
import SkillComponent from './components/skill-component.vue'
import FooterComponent from './components/footer-component.vue'
</script>

<style scoped>
</style>
