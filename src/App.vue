<template>
  <div class="page-header">
    <a id="menu-icon" class="menu-icon" @click="onMenuClick()">
      <i class="fa fa-bars"></i>
    </a>

    <div id="navigation-bar" class="nav-bar">
      <a class="link" href="#particles-js" data-scroll> PKH Portfolio </a>
      <a class="link" href="#about" data-scroll>About Me</a>
      <a class="link" href="#projects" data-scroll>Projects</a>
    </div>
  </div>
  <div id="particles-js">
    <div class="header">
      <h1>
        <span class="site-title">프론트엔드 개발자 포트폴리오</span>
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
            <img
              src="../public/assets/img/jpg/myImag.jpg"
              alt="Professional Me"
              width="20%"
              style="border-radius: 50%;border: 7px solid #fff;"
            />
          </picture>
          <p>
            뭐 임마
          </p>
        </div>
    </section>
  </div>

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

      <div class="user-projects">
        <div class="images-right">
          <picture>
            <source type="image/webp" srcset="../public/assets/img/webp/Personal-Resume-Website.webp" alt="Personal Website" />
            <img alt="Personal Website" src="../public/assets/img/jpg/Personal-Resume-Website.jpg" />
          </picture>
        </div>
        <div class="contents" style="text-align: center">
          <h3>Personal Website</h3>
          <div>
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
              src="https://unpkg.com/simple-icons@3.4.0/icons/bootstrap.svg"
              style="filter: invert(24%) sepia(14%) saturate(2270%) hue-rotate(222deg) brightness(102%) contrast(90%)"
            />
            &nbsp;
            <img height="32" width="32" src="https://unpkg.com/simple-icons@3.4.0/icons/github.svg" />
          </div>
          <p style="text-align: justify">
            I developed and designed a website using ReactJS and Bootstrap, hosted on Github Pages, to showcase my web
            presence, story, work experience, education, projects, and achievements in an interactive and
            visually-appealing format.
          </p>
          <a class="project-link" target="_blank" href="https://www.adityavsingh.com/">Check it out!</a>
        </div>
      </div>

      <!-- User Project #2: Summer 2020 Project -->
      <div class="user-projects">
        <div class="images-left">
          <picture>
            <source type="image/webp" srcset="../public/assets/img/webp/Perpetual-Crusades.webp" alt="Perpetual Crusades" />
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
            I created a two-player online dice-based board game with a theme loosely set around Dungeons & Dragons. It
            was developed as a submission for Penn Apps XXI, using ReactJS and CSS Grid Layouts for design and hosted on
            GitHub Pages.
          </p>
          <a class="project-link" target="_blank" href="https://github.com/AVS1508/Summer-2020-Project"
            >Check it out!</a
          >
        </div>
      </div>

      <!-- User Project #3: COVID-19 Tracker App -->
      <div class="user-projects">
        <div class="images-right">
          <picture>
            <source type="image/webp" srcset="../public/assets/img/webp/COVID19-Tracker-App.webp" alt="COVID-19 Tracker App" />
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
            I created a web application for tracking the spread of COVID-19. Using Johns Hopkins University Center For
            Systems Science and Engineering API, the website processes the COVID-19 data to create statistical
            projections through graphs and charts.
          </p>
          <a class="project-link" target="_blank" href="https://www.adityavsingh.com/covid19-tracker-app">
            Check it out!
          </a>
        </div>
      </div>

      <!-- Use Project #4: Valuto: Account Management System -->
      <div class="user-projects">
        <div class="images-left">
          <picture>
            <source
              type="image/webp"
              srcset="../public/assets/img/webp/Valuto-Account-Management.webp"
              alt="Valuto: Account Management System"
            />
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
            I developed a CLI system for accounting management and financial statement maintenance. The purpose of the
            system is to maintain a record of the funds received, used, disseminated and donated by an organization.
            Details of transactions and maintenance of a budget and tallying of current balance/inventory in cash/kind
            is incorporated in this system.
          </p>
          <a class="project-link" target="_blank" href="https://github.com/AVS1508/Valuto-Account-Management-System">
            Check it out!
          </a>
        </div>
      </div>
    </section>
  </div>

  <footer class="footer">
    <p>&copy; 2023. Park Kyung Ho. All rights reserved.</p>
  </footer>
</template>

<script>
export default {
  name: 'App',
}
</script>

<script setup>
// import { ref } from 'vue';
// const activeLink = ref('HOME');

const onMenuClick = () =>{
  const navbar = document.getElementById('navigation-bar');
  const responsive_class_name = 'responsive'

  navbar.classList.toggle(responsive_class_name)
}

</script>

<style>

</style>
