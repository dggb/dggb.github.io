<template>
  <div style="background-color:#f5f5f5">
    <section id="projects" style="padding-top:40px">
      <div class="user-details">
        <div class="section_table_style">
          <div class="section_title_style" style="color:#000000;">PROJECTS</div>
          
          <a href="#projects" data-scroll>
            <div class="link_image">
            <img src="../../public/assets/img/png/link.png" style="width: 100%;">
          </div>
          </a>
        </div>
      </div>
    </section>
    <section id="portfolio" class="bg-light-gray">
      <div class="container">
          <div class="row">

              <div class="col-md-4 col-sm-6 portfolio-item">
                  <a class="portfolio-link" href="#">
                      <div class="portfolio-hover">
                          <div class="portfolio-hover-content">
                              <i class="fa fa-plus fa-3x"></i>
                          </div>
                      </div>
                      <img src="../../public/assets/img/png/popo.png" class="projects_img_style" alt="" style="width: 100%;">
                  </a>
                  <div class="portfolio-caption">
                      <h4 style="font-weight:bold">개인 포트폴리오 사이트</h4>
                      <div style="margin-top: 1rem;">
                        <img height="32" width="32" src="https://unpkg.com/simple-icons@3.4.0/icons/javascript.svg" style="filter: invert(96%) sepia(47%) saturate(4151%) hue-rotate(338deg) brightness(100%) contrast(95%)">
                        &nbsp;
                        <img height="32" width="32" src="../../public/assets/img/png/vue.png">
                        &nbsp;
                        <img height="32" width="32" src="https://unpkg.com/simple-icons@3.4.0/icons/bootstrap.svg" style="filter: invert(24%) sepia(14%) saturate(2270%) hue-rotate(222deg) brightness(102%) contrast(90%)">
                        &nbsp;
                        <a href="https://github.com/dggb/dggb.github.io" target='_blank'><img height="32" width="32" src="../../public/assets/img/png/github.png"></a>
                      </div>
                  </div>
              </div>

              <div class="col-md-4 col-sm-6 portfolio-item">
                  <a class="portfolio-link" href="https://dggb.github.io/cardgame/" target='_blank'>
                      <div class="portfolio-hover">
                          <div class="portfolio-hover-content">
                              <i class="fa fa-plus fa-3x"></i>
                          </div>
                      </div>
                      <img src="../../public/assets/img/png/cardGame.png" class="projects_img_style" alt="">
                  </a>
                  <div class="portfolio-caption">
                      <h4 style="font-weight:bold">카드 게임</h4>
                      <div style="margin-top: 1rem;">
                        <img height="32" width="32" src="https://unpkg.com/simple-icons@3.4.0/icons/javascript.svg" style="filter: invert(96%) sepia(47%) saturate(4151%) hue-rotate(338deg) brightness(100%) contrast(95%)">
                        &nbsp;
                        <img height="32" width="32" src="../../public/assets/img/png/vue.png">
                        &nbsp;
                        <a href="https://github.com/dggb/cardgame" target='_blank'><img height="32" width="32" src="../../public/assets/img/png/github.png"></a>
                        </div>
                  </div>
              </div>

              <div class="col-md-4 col-sm-6 portfolio-item">
                  <a class="portfolio-link" href="https://dggb.github.io/wordlegame/#/" target='_blank'>
                      <div class="portfolio-hover">
                          <div class="portfolio-hover-content">
                              <i class="fa fa-plus fa-3x"></i>
                          </div>
                      </div>
                      <img src="../../public/assets/img/png/wordlegame.png" class="projects_img_style" alt="">
                  </a>
                  <div class="portfolio-caption">
                      <h4 style="font-weight:bold">워들 게임</h4>
                      <div style="margin-top: 1rem;">
                        <img height="32" width="32" src="https://unpkg.com/simple-icons@3.4.0/icons/javascript.svg" style="filter: invert(96%) sepia(47%) saturate(4151%) hue-rotate(338deg) brightness(100%) contrast(95%)">
                        &nbsp;
                        <img height="32" width="32" src="../../public/assets/img/png/vuetify.png">
                        &nbsp;
                        <img height="32" width="32" src="../../public/assets/img/png/vue.png">
                        &nbsp;
                        <a href="https://github.com/dggb/wordlegame" target='_blank'><img height="32" width="32" src="../../public/assets/img/png/github.png"></a>
                      </div>
                  </div>
              </div>

              <div class="col-md-4 col-sm-6 portfolio-item">
                  <a class="portfolio-link" data-toggle="modal" @click="modal('semi')">
                      <div class="portfolio-hover">
                          <div class="portfolio-hover-content">
                              <i class="fa fa-plus fa-3x"></i>
                          </div>
                      </div>
                      <img src="../../public/assets/img/png/semi.png" class="projects_img_style" alt="" style="width: 100%;">
                  </a>
                  <div class="portfolio-caption">
                      <h4 style="font-weight:bold">구인구직 사이트 오늘 뭐해?</h4>
                      <div style="margin-top: 1rem;">
                        <img height="32" width="32" src="../../public/assets/img/png/java.png">
                        &nbsp;
                        <img height="32" width="32" src="https://unpkg.com/simple-icons@3.4.0/icons/javascript.svg" style="filter: invert(96%) sepia(47%) saturate(4151%) hue-rotate(338deg) brightness(100%) contrast(95%)">
                        &nbsp;
                        <img height="32" width="32" src="https://unpkg.com/simple-icons@3.4.0/icons/bootstrap.svg" style="filter: invert(24%) sepia(14%) saturate(2270%) hue-rotate(222deg) brightness(102%) contrast(90%)">
                        &nbsp;
                        <img height="32" width="32" src="../../public/assets/img/png/github.png">
                      </div>
                  </div>
              </div>

              <div class="col-md-4 col-sm-6 portfolio-item">
                  <a class="portfolio-link" data-toggle="modal" @click="modal('semi')">
                      <div class="portfolio-hover">
                          <div class="portfolio-hover-content">
                              <i class="fa fa-plus fa-3x"></i>
                          </div>
                      </div>
                      <img src="../../public/assets/img/png/sellpie.png" class="projects_img_style" alt="" style="width: 100%;background-color:wheat;object-fit:contain">
                  </a>
                  <div class="portfolio-caption">
                      <h4 style="font-weight:bold">재능 거래 플랫폼 SellPie</h4>
                      <div style="margin-top: 1rem;">
                        <img height="32" width="32" src="../../public/assets/img/png/java.png">
                        &nbsp;
                        <img height="32" width="32" src="https://unpkg.com/simple-icons@3.4.0/icons/javascript.svg" style="filter: invert(96%) sepia(47%) saturate(4151%) hue-rotate(338deg) brightness(100%) contrast(95%)">
                        &nbsp;
                        <img height="32" width="32" src="https://unpkg.com/simple-icons@3.4.0/icons/bootstrap.svg" style="filter: invert(24%) sepia(14%) saturate(2270%) hue-rotate(222deg) brightness(102%) contrast(90%)">
                        &nbsp;
                        <img height="32" width="32" src="../../public/assets/img/png/github.png">
                      </div>
                  </div>
              </div>
          </div>
      </div>
    </section>
  </div>

  <ModalComponent ref="refModal"></ModalComponent>
</template>

<script>
export default {
  name: 'project-component'
}
</script>

<script setup>
import ModalComponent from './modal-component.vue'
import {ref} from 'vue';
const refModal = ref(null);

const modal = (item) => {

  alert('준비 중입니다!')
    // refModal.value.open(item)
}

</script>
<style scoped>

</style>
