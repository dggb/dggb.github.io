<template>
  <div style="background-color:#f5f5f5">
    <section id="projects" style="padding-top:45px">
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
                  <a class="portfolio-link" data-toggle="modal" href="#">
                      <div class="portfolio-hover">
                          <div class="portfolio-hover-content">
                              <i class="fa fa-plus fa-3x"></i>
                          </div>
                      </div>
                      <img src="../../public/assets/img/jpg/COVID19-Tracker-App.jpg" class="projects_img_style" alt="">
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
                      <img src="../../public/assets/img/jpg/Perpetual-Crusades.jpg" class="projects_img_style" alt="">
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
                      <img src="../../public/assets/img/jpg/Valuto-Account-Management.jpg" class="projects_img_style" alt="">
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
</template>

<script>
export default {
  name: 'ProjectComponent'
}
</script>

<style scoped>

</style>
