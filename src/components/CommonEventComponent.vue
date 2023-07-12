<template>
  <!-- 스크롤 시 오른쪽 하단 버튼 이벤트 -->
  <a id="scrollToTopButton" href="#" style="display: none;" data-scroll @click="scrollToTop" v-show="showScrollButton">
    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-arrow-up-square" viewBox="0 0 16 16">
      <path fill-rule="evenodd" d="M15 2a1 1 0 0 0-1-1H2a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1V2zM0 2a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V2zm8.5 9.5a.5.5 0 0 1-1 0V5.707L5.354 7.854a.5.5 0 1 1-.708-.708l3-3a.5.5 0 0 1 .708 0l3 3a.5.5 0 0 1-.708.708L8.5 5.707V11.5z"/>
    </svg>
  </a>
    
  <!-- navBar -->
  <nav class="navbar navbar-default navbar-fixed-top" id="navbarStyle">
      <div class="container">
          <div class="navbar-header page-scroll">
              <button type="button" class="navbar-toggle collapsed" @click="toggleData">
                  <span class="sr-only">Toggle navigation</span>
                  <span class="icon-bar"></span>
                  <span class="icon-bar"></span>
                  <span class="icon-bar"></span>
              </button>
              <a class="navbar-brand page-scroll" href="#" style="font-weight:bold" data-scroll :class="{ 'titleColor': showHamburger }">PKH Portfolio</a>
          </div>

          <div class="collapse navbar-collapse" :class="{ 'in': isToggle }">
              <ul class="nav navbar-nav navbar-right">                    
                  <li>
                      <a class="page-scroll" href="#about" data-scroll @click="closeToggle">About</a>
                  </li>
                  <li>
                      <a class="page-scroll" href="#projects" data-scroll @click="closeToggle">Portfolio</a>
                  </li>
              </ul>
          </div>
      </div>
  </nav>
</template>

<script>
export default {
  name: 'CommonEventComponent'
}
</script>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';

const showScrollButton = ref(false);
const isToggle = ref(false);
const showHamburger = ref(false);

const toggleData = () => {
  isToggle.value = !isToggle.value;
};

const handleScroll = () => {
  const navbar = document.getElementById("navbarStyle");
  const screenWidth = window.innerWidth < 768;
  const isScrolled = window.pageYOffset > 100;

  showScrollButton.value = isScrolled;

  if (screenWidth) {
    navbar.className = `navbar navbar-default navbar-fixed-top navbar-scrolled`;
    showHamburger.value = true;
  } else {
    navbar.className = `navbar navbar-default navbar-fixed-top ${isScrolled ? "navbar-scrolled" : "navbar-noScrolled"}`;
    showHamburger.value = isScrolled;
  }
};

const handleResize = () => {
  handleScroll();
};

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
  window.addEventListener('resize', handleResize);
});

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll);
  window.removeEventListener('resize', handleResize); 
});

const closeToggle = () => {
  isToggle.value = false;
}
</script>

<style scoped>

</style>
