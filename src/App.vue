<template>
  <div>
    <!-- 오른쪽 하단 버튼 이벤트 -->
    <a id="scrollToTopButton" href="#" style="display: none;" data-scroll @click="scrollToTop" v-show="showScrollButton">
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-arrow-up-square" viewBox="0 0 16 16">
        <path fill-rule="evenodd" d="M15 2a1 1 0 0 0-1-1H2a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1V2zM0 2a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V2zm8.5 9.5a.5.5 0 0 1-1 0V5.707L5.354 7.854a.5.5 0 1 1-.708-.708l3-3a.5.5 0 0 1 .708 0l3 3a.5.5 0 0 1-.708.708L8.5 5.707V11.5z"/>
      </svg>
    </a>
    
    <!-- navBar 페이지 -->
    <nav class="navbar navbar-default navbar-fixed-top" id="navbarStyle">
        <div class="container">
            <div class="navbar-header page-scroll">
                <button type="button" class="navbar-toggle collapsed" @click="toggleData">
                    <span class="sr-only">Toggle navigation</span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                </button>
                <a class="navbar-brand page-scroll" href="#" style="font-weight:bold" data-scroll :class="{ 'titleColor': showScrollButton }">PKH Portfolio</a>
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
    
    <!-- header 페이지 -->
    <div id="particles-js">
      <div class="header">
        <h1 style="font-weight:bold">
          <span class="site-title">프론트엔드 개발자</span>
          <span class="site-description">- 박경호 -</span>
        </h1>
        <div class="header-icons">
          <!-- <a aria-label="My LinkedIn Profile" target="_blank" href="https://www.linkedin.com/in/avs1508/">
            <i class="icon fa fa-linkedin" aria-hidden="true"></i>
          </a> -->
          <!-- <a aria-label="My Résumé" target="_blank" href="https://www.adityavsingh.com/resume.html">
            <i class="icon fa fa fa-file-pdf-o" aria-hidden="true"></i>
          </a>
          <a aria-label="Send Email" href="mailto:avsingh@umass.edu" target="_blank"
            ><i class="icon fa fa-envelope"></i
          ></a> -->
          <a aria-label="My Github Profile" target="_blank" href="https://github.com/dggb">
            <i class="icon fa fa-github-alt" aria-hidden="true"></i>
          </a>

        </div>
        <div class="header-links">
          <a class="link" href="#about" data-scroll>About Me</a>
          <a class="link" href="#projects" data-scroll>Projects</a>
        </div>
      </div>
      <a class="down" href="#about" data-scroll><i class="icon fa fa-chevron-down" aria-hidden="true"></i></a>
    </div>

    <!-- about me 페이지 -->
    <div id="about" style="padding: 30px;"></div>
    <div style="background-color:white">
      <section >
          <div class="user-details">
            <div class="section_table_style">
              <div class="section_title_style" style="color:#000000;">ABOUT ME</div>
              
              <a href="#about" data-scroll>
                <div class="link_image">
                <img src="../public/assets/img/png/link.png" style="width: 100%;">
              </div>
              </a>
            </div>
            <picture>
              <!-- 내 사진 -->
              <img src="../public/assets/img/jpg/myImag.jpg" class="myImg"/>
            </picture>

            <div class="about_div_style">
              <div class="about_child_style">
                <div class="box_size_style">
                  <div class="box_info_style">
                    <div class="box_image_style">
                      <img src="../public/assets/img/png/user.png" style="width: 100%; vertical-align:middle">
                    </div>

                    <div>
                      <div class="box_title_style">이름</div>
                      <div class="box_item_style">박경호</div>
                    </div>
                  </div>
                </div>
                <div class="box_size_style">
                  <div class="box_info_style">
                    <div class="box_image_style">
                      <img src="../public/assets/img/png/calendar.png" style="width: 100%; vertical-align:middle">
                    </div>

                    <div>
                      <div class="box_title_style">생년월일</div>
                      <div class="box_item_style">93.12.14</div>
                    </div>
                  </div>
                </div>
                <div class="box_size_style">
                  <div class="box_info_style">
                    <div class="box_image_style">
                      <img src="../public/assets/img/png/location.png" style="width: 100%; vertical-align:middle">
                    </div>

                    <div>
                      <div class="box_title_style">주소지</div>
                      <div class="box_item_style">서울특별시 송파구</div>
                    </div>
                  </div>
                </div>
                <div class="box_size_style">
                  <div class="box_info_style">
                    <div class="box_image_style">
                      <img src="../public/assets/img/png/phone.png" style="width: 100%; vertical-align:middle">
                    </div>

                    <div>
                      <div class="box_title_style">연락처</div>
                      <div class="box_item_style">010-4013-4685</div>
                    </div>
                  </div>
                </div>
                <div class="box_size_style">
                  <div class="box_info_style">
                    <div class="box_image_style">
                      <img src="../public/assets/img/png/email.png" style="width: 100%; vertical-align:middle">
                    </div>

                    <div>
                      <div class="box_title_style">이메일</div>
                      <div class="box_item_style">dggb2@naver.com</div>
                    </div>
                  </div>
                </div>
                <div class="box_size_style">
                  <div class="box_info_style">
                    <div class="box_image_style">
                      <img src="../public/assets/img/png/Education.png" style="width: 100%; vertical-align:middle">
                    </div>

                    <div>
                      <div class="box_title_style">학력</div>
                      <div class="box_item_style">방송통신대학교<br>(컴퓨터과학과)<br>동서울대학교<br>(소프트웨어과)</div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="about_footer_style">* 문의 사항이 있으시면&nbsp;
                <br class="about_footer_br_style">
                위 연락처/이메일로 연락 해주세요.
              </div>
            </div>
          </div>
      </section>
    </div>

    <!-- projects 페이지 -->
    <div style="background-color:#f5f5f5">
      <section id="projects" style="padding-top:45px">
        <div class="user-details">
          <div class="section_table_style">
            <div class="section_title_style" style="color:#000000;">PROJECTS</div>
            
            <a href="#projects" data-scroll>
              <div class="link_image">
              <img src="../public/assets/img/png/link.png" style="width: 100%;">
            </div>
            </a>
          </div>
        </div>
      </section>
      <section id="portfolio" class="bg-light-gray">
        <div class="container">
            <div class="row">
                <div class="col-md-4 col-sm-6 portfolio-item">
                    <a class="portfolio-link" data-toggle="modal" href="#">
                        <div class="portfolio-hover">
                            <div class="portfolio-hover-content">
                                <i class="fa fa-plus fa-3x"></i>
                            </div>
                        </div>
                        <img src="../public/assets/img/jpg/COVID19-Tracker-App.jpg" class="projects_img_style" alt="">
                    </a>
                    <div class="portfolio-caption">
                        <h4 style="font-weight:bold">코로나 어플</h4>
                        <p class="text-muted">뭘 했을까</p>
                    </div>
                </div>

                <div class="col-md-4 col-sm-6 portfolio-item">
                    <a class="portfolio-link" data-toggle="modal" href="#">
                        <div class="portfolio-hover">
                            <div class="portfolio-hover-content">
                                <i class="fa fa-plus fa-3x"></i>
                            </div>
                        </div>
                        <img src="../public/assets/img/jpg/Perpetual-Crusades.jpg" class="projects_img_style" alt="">
                    </a>
                    <div class="portfolio-caption">
                        <h4 style="font-weight:bold">게임 사이트</h4>
                        <p class="text-muted">만 들었을까</p>
                    </div>
                </div>

                <div class="col-md-4 col-sm-6 portfolio-item">
                    <a class="portfolio-link" data-toggle="modal" href="#">
                        <div class="portfolio-hover">
                            <div class="portfolio-hover-content">
                                <i class="fa fa-plus fa-3x"></i>
                            </div>
                        </div>
                        <img src="../public/assets/img/jpg/Valuto-Account-Management.jpg" class="projects_img_style" alt="">
                    </a>
                    <div class="portfolio-caption">
                        <h4 style="font-weight:bold">코드 테스트</h4>
                        <p class="text-muted">하긴 했겠지</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    </div>

    <!-- footer -->
    <footer class="footer">
      <p>&copy; 2023. Park Kyung Ho. All rights reserved.</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
}
</script>

<script setup>

import { ref, onMounted, onBeforeUnmount } from 'vue';

const showScrollButton = ref(false);
const isToggle = ref(false);

const toggleData = () => {
  isToggle.value = !isToggle.value;
};

const handleScroll = () => {
  const navbar = document.getElementById("navbarStyle");

  if (window.pageYOffset > 100) {
    showScrollButton.value = true;
    navbar.className = "navbar navbar-default navbar-fixed-top navbar-scrolled";
  } else {
    if(window.innerWidth < 768){
      showScrollButton.value = true;
      navbar.className = "navbar navbar-default navbar-fixed-top navbar-scrolled";
    }else{
      showScrollButton.value = false;
      navbar.className = "navbar navbar-default navbar-fixed-top navbar-noScrolled";
    }
  }
};

const handleResize = () => {
  const navbar = document.getElementById("navbarStyle");

  if (window.innerWidth < 768) {
    showScrollButton.value = true;
    navbar.className = "navbar navbar-default navbar-fixed-top navbar-scrolled";
  } else {
    if(window.pageYOffset > 100){
      showScrollButton.value = true;
      navbar.className = "navbar navbar-default navbar-fixed-top navbar-scrolled";
    }else{
      showScrollButton.value = false;
      navbar.className = "navbar navbar-default navbar-fixed-top navbar-noScrolled";
    }
  }
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

<style>

</style>
