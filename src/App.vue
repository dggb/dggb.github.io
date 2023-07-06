<template>
  <div>
    <!-- 오른쪽 하단 버튼 이벤트 -->
    <a id="scrollToTopButton" href="#" style="display: none;" data-scroll @click="scrollToTop" v-show="showScrollButton">
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-arrow-up-square" viewBox="0 0 16 16">
        <path fill-rule="evenodd" d="M15 2a1 1 0 0 0-1-1H2a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1V2zM0 2a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V2zm8.5 9.5a.5.5 0 0 1-1 0V5.707L5.354 7.854a.5.5 0 1 1-.708-.708l3-3a.5.5 0 0 1 .708 0l3 3a.5.5 0 0 1-.708.708L8.5 5.707V11.5z"/>
      </svg>
    </a>
    
    <!-- navBar 페이지 -->
    <div class="page-navBar">
      <a id="menu-icon" class="menu-icon" @click="onMenuClick()">
        <i class="fa fa-bars"></i>
      </a>

      <div id="navigation-bar" class="nav-bar">
        <a class="link" href="#particles-js" data-scroll> PKH Portfolio </a>
        <a class="link" href="#about" data-scroll>About Me</a>
        <a class="link" href="#projects" data-scroll>Projects</a>
      </div>
    </div>
    
    <!-- header 페이지 -->
    <div id="particles-js">
      <div class="header">
        <h1>
          <span class="site-title">프론트엔드 개발자</span>
          <span class="site-description">- 박경호 -</span>
        </h1>
        <div class="header-icons">
          <!-- <a aria-label="My LinkedIn Profile" target="_blank" href="https://www.linkedin.com/in/avs1508/">
            <i class="icon fa fa-linkedin" aria-hidden="true"></i>
          </a> -->
          <a aria-label="My Github Profile" target="_blank" href="https://github.com/dggb">
            <i class="icon fa fa-github-alt" aria-hidden="true"></i>
          </a>
          <!-- <a aria-label="My Résumé" target="_blank" href="https://www.adityavsingh.com/resume.html">
            <i class="icon fa fa fa-file-pdf-o" aria-hidden="true"></i>
          </a>
          <a aria-label="Send Email" href="mailto:avsingh@umass.edu" target="_blank"
            ><i class="icon fa fa-envelope"></i
          ></a> -->
        </div>
        <div class="header-links">
          <a class="link" href="#about" data-scroll>About Me</a>
          <a class="link" href="#projects" data-scroll>Projects</a>
        </div>
      </div>
      <a class="down" href="#about" data-scroll><i class="icon fa fa-chevron-down" aria-hidden="true"></i></a>
    </div>

    <!-- about me 페이지 -->
    <div style="background-color:white">
      <section id="about">
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
              <img
                src="../public/assets/img/jpg/myImag.jpg"
                alt="Professional Me"
                width="20%"
                style="border-radius: 50%;border: 7px solid #fff;"
              />
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
      <section id="projects">
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

        <!-- User Project #2: Summer 2020 Project -->
        <div class="user-projects">
          <div class="images-left">
            <picture>
              <img alt="Perpetual Crusades" src="../public/assets/img/jpg/Perpetual-Crusades.jpg" />
            </picture>
          </div>
          <div class="contents-right" style="text-align: center">
            <h3>Perpetual Crusades</h3>
            <img
              height="32"
              width="32"
              src="https://unpkg.com/simple-icons@3.4.0/icons/react.svg"
              style="filter: invert(73%) sepia(74%) saturate(1552%) hue-rotate(169deg) brightness(109%) contrast(97%)"
            />
            &nbsp;
            <img
              height="32"
              width="32"
              src="https://unpkg.com/simple-icons@3.4.0/icons/css3.svg"
              style="filter: invert(33%) sepia(29%) saturate(3844%) hue-rotate(184deg) brightness(90%) contrast(84%)"
            />
            &nbsp;
            <img height="32" width="32" src="https://unpkg.com/simple-icons@3.4.0/icons/github.svg" />
            <p style="text-align: justify">
              만들고 있는 중 입니다.
            </p>
            <a class="project-link" target="_blank">자세히 보기!</a
            >
          </div>
        </div>

        <!-- User Project #3: COVID-19 Tracker App -->
        <div class="user-projects">
          <div class="images-right">
            <picture>
              <img alt="COVID-19 Tracker App" src="../public/assets/img/jpg/COVID19-Tracker-App.jpg" />
            </picture>
          </div>
          <div class="contents" style="text-align: center">
            <h3>COVID-19 Tracker App</h3>
            <div>
              <img
                height="32"
                width="32"
                src="https://unpkg.com/simple-icons@3.4.0/icons/javascript.svg"
                style="filter: invert(96%) sepia(47%) saturate(4151%) hue-rotate(338deg) brightness(100%) contrast(95%)"
              />
            </div>
            <p style="text-align: justify">
              만들고 있는 중 입니다.
            </p>
            <a class="project-link" target="_blank">
              자세히 보기!
            </a>
          </div>
        </div>

        <!-- Use Project #4: Valuto: Account Management System -->
        <div class="user-projects">
          <div class="images-left">
            <picture>
              <img alt="Valuto: Account Management System" src="../public/assets/img/jpg/Valuto-Account-Management.jpg" />
            </picture>
          </div>
          <div class="contents-right" style="text-align: center">
            <h3>Valuto: Account Management System</h3>
            <div>
              <img
                height="32"
                width="32"
                src="https://unpkg.com/simple-icons@3.4.0/icons/cplusplus.svg"
                style="filter: invert(22%) sepia(77%) saturate(1486%) hue-rotate(183deg) brightness(101%) contrast(103%)"
              />
            </div>
            <p style="text-align: justify">
              만들고 있는 중 입니다.
            </p>
            <a class="project-link" target="_blank">
              자세히 보기!
            </a>
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
// const activeLink = ref('HOME');

const showScrollButton = ref(false);

const handleScroll = () => {
  if (window.pageYOffset > 100) {
    showScrollButton.value = true;
  } else {
    showScrollButton.value = false;
  }
};

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll);
});

const onMenuClick = () =>{
  const navbar = document.getElementById('navigation-bar');
  const responsive_class_name = 'responsive'

  navbar.classList.toggle(responsive_class_name)
}

</script>

<style>

</style>
