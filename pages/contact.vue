/* eslint-disable no-undef */
<template>
  <div>
    <!-- Start Content Page -->
    <div class="container-fluid bg-light py-5">
      <div class="col-md-6 m-auto text-center">
        <h1 class="h1">
          Contact Us
        </h1>
        <p>
          Apabila terdapat pertanyaan, anda dapat menghubungi kami melalui formulir berikut
        </p>
      </div>
    </div>

    <!-- Start Map -->
    <div class="col-12 mt-5 mx-2 my-1">
      <div class="col-md-8 mx-auto">
        <div class="card">
          <div class="card-header">
            <div class="card-title text-center">Maps</div>
          </div>
          <div class="card-body">
            <div id="mapid" style="height: 300px;" />
          </div>
        </div>
      </div>
    </div>
    <!-- <div id="map-wrap" style="height: 100vh">
      <client-only>
        <l-map :zoom=13 :center="[-23.013104, -43.394365, 13]">
          <l-tile-layer
            url="https://api.mapbox.com/styles/v1/{id}/tiles/{z}/{x}/{y}?access_token=pk.eyJ1IjoibWFwYm94IiwiYSI6ImNpejY4NXVycTA2emYycXBndHRqcmZ3N3gifQ.rJcFIG214AriISLbB6B5aw">
          </l-tile-layer>
          <l-marker :lat-lng="[-23.013104, -43.394365, 13]"></l-marker>
        </l-map>
      </client-only>
    </div> -->
    <!-- Ena Map -->

    <!-- Start Contact -->
    <div class="container py-5">
      <div class="row py-5">
        <form class="col-md-9 m-auto" method="post" role="form">
          <div class="row">
            <div class="form-group col-md-6 mb-3">
              <label for="inputname">Name</label>
              <input id="name" type="text" class="form-control mt-1" name="name" placeholder="Name">
            </div>
            <div class="form-group col-md-6 mb-3">
              <label for="inputemail">Email</label>
              <input id="email" type="email" class="form-control mt-1" name="email" placeholder="Email">
            </div>
          </div>
          <div class="mb-3">
            <label for="inputsubject">Subject</label>
            <input id="subject" type="text" class="form-control mt-1" name="subject" placeholder="Subject">
          </div>
          <div class="mb-3">
            <label for="inputmessage">Message</label>
            <textarea id="message" class="form-control mt-1" name="message" placeholder="Message" rows="8" />
            </div>
          <div class="row">
            <div class="col text-end mt-2">
              <button type="submit" class="btn btn-success btn-lg px-3">
                Let’s Talk
              </button>
            </div>
          </div>
        </form>
      </div>
    </div>
    <!-- End Contact -->
  </div>
</template>
<script>
// import Vue from 'vue';
// import { LMap, LTileLayer, LMarker } from 'vue2-leaflet';

// Vue.component('l-map', LMap);
// Vue.component('l-tile-layer', LTileLayer);
// Vue.component('l-marker', LMarker);
export default {
  name: 'TambahPage',
  layout: 'MainDefault',
  head(){
    return {
      script: [
        {
          hid: 'leaflet',
          src: 'https://unpkg.com/leaflet@1.7.1/dist/leaflet.js',
          defer: true,
          // Changed after script load
          }
      ],
    }
  },
  mounted () {
    // eslint-disable-next-line no-undef
    const mymap = L.map('mapid').setView([-7.048711, 110.421527, 13], 13)

    // eslint-disable-next-line no-undef
    L.tileLayer('https://api.mapbox.com/styles/v1/{id}/tiles/{z}/{x}/{y}?access_token=pk.eyJ1IjoibWFwYm94IiwiYSI6ImNpejY4NXVycTA2emYycXBndHRqcmZ3N3gifQ.rJcFIG214AriISLbB6B5aw', {
      maxZoom: 18,
      attribution: '<a href="https://www.harimbawastore.my.id/">Harimbawa Store</a>',
      id: 'mapbox/streets-v11',
      tileSize: 512,
      zoomOffset: -1
    }).addTo(mymap)

    // eslint-disable-next-line no-undef
    L.marker([-7.048711, 110.421527, 13]).addTo(mymap)
      .bindPopup('<b>Harimbawa</b> Store <br />Location.').openPopup()

    mymap.scrollWheelZoom.disable()
    mymap.touchZoom.disable()
  }
}
</script>
