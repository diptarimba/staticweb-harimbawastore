<template>
  <div>
    <section class="bg-success py-5">
      <div class="container">
        <div class="row align-items-center py-5">
          <div class="col-md-8 text-white">
            <h1>About Us</h1>
            <p>
              Harimbawa Store menyediakan berbagai macam service yang dapat membantu anda dalam membuat, mengelola, dan mengembangkan website anda.

              Kami telah berpengalaman dalam membuat website lebih dari 2 tahun.
            </p>
          </div>
          <div class="col-md-4">
            <img src="/img/about-hero.svg" alt="About Hero">
          </div>
        </div>
      </div>
    </section>
    <!-- Close Banner -->

    <!-- Start Section -->
    <section class="container py-5">
      <div class="row text-center pt-5 pb-3">
        <div class="col-lg-6 m-auto">
          <h1 class="h1">
            Our Services
          </h1>
          <p>
            Kami memiliki 4 komponen utama dalam melakukan bisnis, yaitu
          </p>
        </div>
      </div>
      <div class="row">
        <div v-for="(value, key) in serviceData" :key="key" class="col-md-6 col-lg-3 pb-5">
          <div class="h-100 py-5 services-icon-wap shadow">
            <div class="h1 text-success text-center">
              <i :class="value.icon" />
            </div>
            <h2 class="h5 mt-4 text-center">
              {{ value.title }}
            </h2>
          </div>
        </div>
      </div>
    </section>
    <!-- End Section -->

    <!-- Start Brands -->
    <section class="bg-light py-5">
      <div class="container my-4">
        <div class="row text-center py-3">
          <div class="col-lg-6 m-auto">
            <h1 class="h1">
              Supported by
            </h1>
            <p>
              Framework, database, maupun bahasa yang bisa kami terapkan.
            </p>
          </div>
          <div class="col-lg-9 m-auto tempaltemo-carousel">
            <div class="row d-flex flex-row">
              <!--Controls-->
              <div class="col-1 align-self-center">
                <a class="h1" href="#templatemo-slide-brand" role="button" data-bs-slide="prev">
                  <i class="text-light fas fa-chevron-left" />
                </a>
              </div>
              <!--End Controls-->

              <!--Carousel Wrapper-->
              <div class="col">
                <div id="templatemo-slide-brand" class="carousel slide carousel-multi-item pt-2 pt-md-0" data-bs-ride="carousel">
                  <!--Slides-->
                  <div class="carousel-inner product-links-wap" role="listbox">
                    <!--First slide-->
                    <div class="carousel-item active">
                      <div class="row">
                        <div v-for="(value, key) in caraouselData" :key="key" class="col-3 p-md-5">
                          <a href="#"><img class="img-fluid brand-img" :src="'/img/' + value" alt="Brand Logo"></a>
                        </div>
                      </div>
                    </div>
                    <!--End First slide-->

                    <!--Second slide-->
                    <div class="carousel-item">
                      <div class="row">
                        <div v-for="(value, key) in caraouselData" :key="key" class="col-3 p-md-5">
                          <a href="#"><img class="img-fluid brand-img" :src="'/img/' + value" alt="Brand Logo"></a>
                        </div>
                      </div>
                    </div>
                    <!--End Second slide-->

                    <!--Third slide-->
                    <div class="carousel-item">
                      <div class="row">
                        <div v-for="(value, key) in caraouselData" :key="key" class="col-3 p-md-5">
                          <a href="#"><img class="img-fluid brand-img" :src="'/img/' + value" alt="Brand Logo"></a>
                        </div>
                      </div>
                    </div>
                    <!--End Third slide-->
                  </div>
                  <!--End Slides-->
                </div>
              </div>
              <!--End Carousel Wrapper-->

              <!--Controls-->
              <div class="col-1 align-self-center">
                <a class="h1" href="#templatemo-slide-brand" role="button" data-bs-slide="next">
                  <i class="text-light fas fa-chevron-right" />
                </a>
              </div>
              <!--End Controls-->
            </div>
          </div>
        </div>
      </div>
    </section>
    <!--End Brands-->
  </div>
</template>
<script>
export default {
  name: 'AboutPage',
  layout: 'MainDefault',
  data(){
    return {
      caraouselData: [
        'brand_01.png',
        'brand_02.png',
        'brand_03.png',
        'brand_04.png'
      ],
      serviceData: [
        { title: 'Build', icon: 'fa fa-dharmachakra fa-lg'},
        { title: 'Maintenance', icon: 'fas fa-wrench'},
        { title: 'Develop', icon: 'fa fa-tools'},
        { title: 'Backup', icon: 'fa fa-database'}
      ]
    }
  }
}
</script>
