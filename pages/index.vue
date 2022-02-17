<template>
  <div class="container">
    <div class="col-md-12 mx-5 my-5">
      <div class="row justify-content-center">
        <div class="col-md-6">
          <p class="text-center h1 display-1">Portofolio</p>
        </div>
        <div class="col-md-12">
          <div class="row row-cols-1 row-cols-md-2 g-4">
            <div v-for="(value, key) in hompage" :key="key" class="col">
              <div class="card h-100">
                <img :src="'/img/' + value.image " class="card-img-top img-thumbnail" alt="...">
                <div class="card-body">
                  <a :href="value.link" class="h5 card-title nav-link" target="_blank">{{ value.title }}</a>
                  <p class="card-text">{{ value.description }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
  export default {
    name: 'IndexPage',
    layout: 'MainDefault',
    data(){
      return {
        hompage: [
          {
            title: 'Cuan Saham',
            description: 'Website yang dibuat agar ready-to-use untuk menganalisis saham dengan update otomatis',
            image: 'product_1.PNG',
            link: 'https://cuansaham.my.id'
          },
          {
            title: 'Neoducation Management System',
            description: 'Penggunaan website ini digunakan untuk mengelola, mengawasi, dan memantau siswa maupun tentor pada bimbingan belajar neoducationz',
            image: 'product_2.PNG',
            link: 'https://bimbelneuducation.my.id'
          },
          {
            title: 'Yandex Creator',
            description: 'Web Automation saat ini sangat aktif digunakan dalam memanagemen pekerjaan berulang yang bisa dikerjakan otomatis menggunakan programming',
            image: 'product_3.PNG',
            link: 'https://github.com/diptarimba/YandexCreatorJs'
          },
          {
            title: 'Kios Saham Telegram Bot',
            description: 'Analisis saham menggunakan telegram bot untuk menganalisis saham dengan metode tertentu dan juga menampilkan grafik',
            image: 'product_4.PNG',
            link: 'https://t.me/kiosaham_bot'
          },
        ],
      }
    }
  }

</script>
