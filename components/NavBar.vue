<template>
  <div>
    <!-- Start Top Nav -->
    <nav id="templatemo_nav_top" class="navbar navbar-expand-lg bg-dark navbar-light d-none d-lg-block">
      <div class="container text-light">
        <div class="w-100 d-flex justify-content-between">
          <div>
            <i class="fa fa-envelope mx-2" />
            <nuxt-link class="navbar-sm-brand text-light text-decoration-none" to="mailto:diptaharimbawa@gmail.com">
              diptaharimbawa@gmail.com
            </nuxt-link>
            <i class="fa fa-phone mx-2" />
            <nuxt-link class="navbar-sm-brand text-light text-decoration-none" to="tel:089-531-729-222">
              089-531-729-222
            </nuxt-link>
          </div>
          <div>
            <a class="text-light" href="https://github.com/diptarimba" target="_blank" rel="sponsored"><i class="fab fa-github fa-sm fa-fw me-2" /></a>
            <a class="text-light" href="https://www.instagram.com/dpthrw" target="_blank"><i class="fab fa-instagram fa-sm fa-fw me-2" /></a>
            <a class="text-light" href="https://twitter.com/jpmorganid" target="_blank"><i class="fab fa-twitter fa-sm fa-fw me-2" /></a>
            <a class="text-light" href="https://www.linkedin.com/in/dipta-harimbawa/" target="_blank"><i class="fab fa-linkedin fa-sm fa-fw" /></a>
          </div>
        </div>
      </div>
    </nav>
    <!-- Close Top Nav -->

    <!-- Header -->
    <nav class="navbar navbar-expand-lg navbar-light shadow">
      <div class="container d-flex justify-content-between align-items-center">
        <a class="navbar-brand text-success logo h1 align-self-center" href="index.html">
          Harimbawa Store
        </a>

        <button
          class="navbar-toggler border-0"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#templatemo_main_nav"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon" />
        </button>

        <div id="templatemo_main_nav" class="align-self-center collapse navbar-collapse flex-fill  d-lg-flex justify-content-lg-between">
          <div class="flex-fill">
            <ul class="nav navbar-nav d-flex justify-content-between mx-lg-auto">
              <li class="nav-item">
                <nuxt-link class="nav-link" to="/">
                  Home
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link class="nav-link" to="/about">
                  About
                </nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link class="nav-link" to="/contact">
                  Contact
                </nuxt-link>
              </li>
            </ul>
          </div>
          <div class="navbar align-self-center d-flex">
            <div class="d-lg-none flex-sm-fill mt-3 mb-4 col-7 col-sm-auto pr-3">
              <div class="input-group">
                <input id="inputMobileSearch" type="text" class="form-control" placeholder="Search ...">
                <div class="input-group-text">
                  <i class="fa fa-fw fa-search" />
                </div>
              </div>
            </div>
            <!-- <a class="nav-icon d-none d-lg-inline" href="#" data-bs-toggle="modal" data-bs-target="#templatemo_search">
              <i class="fa fa-fw fa-search text-dark mr-2" />
            </a>
            <a class="nav-icon position-relative text-decoration-none" href="#">
              <i class="fa fa-fw fa-cart-arrow-down text-dark mr-1" />
              <span class="position-absolute top-0 left-100 translate-middle badge rounded-pill bg-light text-dark">7</span>
            </a>
            <a class="nav-icon position-relative text-decoration-none" href="#">
              <i class="fa fa-fw fa-user text-dark mr-3" />
              <span class="position-absolute top-0 left-100 translate-middle badge rounded-pill bg-light text-dark">+99</span>
            </a> -->
          </div>
        </div>
      </div>
    </nav>
    <!-- Close Header -->

    <!-- Modal -->
    <div
      id="templatemo_search"
      class="modal fade bg-white"
      tabindex="-1"
      role="dialog"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-lg" role="document">
        <div class="w-100 pt-1 mb-5 text-right">
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close" />
        </div>
        <form action="" method="get" class="modal-content modal-body border-0 p-0">
          <div class="input-group mb-2">
            <input id="inputModalSearch" type="text" class="form-control" name="q" placeholder="Search ...">
            <button type="submit" class="input-group-text bg-success text-light">
              <i class="fa fa-fw fa-search text-white" />
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'NavPage'
}
</script>
