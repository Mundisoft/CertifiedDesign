<template>
  <!--====================  header area ====================-->
  <div class="header-area">
    <div class="header-area__desktop header-area__desktop--default">
      <!--=======  header top bar  =======-->
      <div class="header-top-bar">
        <div class="container">
          <div class="row align-items-center">
            <div class="col-lg-4">
              <!-- top bar left -->
              <div class="top-bar-left-wrapper">
                <div class="social-links social-links--white-topbar d-inline-block">
                  <ul>
                    <li>
                      <a href="//facebook.com" target="_blank">
                        <i class="zmdi zmdi-facebook"></i>
                      </a>
                    </li>
                    <li>
                      <a href="//twitter.com" target="_blank">
                        <i class="zmdi zmdi-twitter"></i>
                      </a>
                    </li>
                    <li>
                      <a href="//vimeo.com" target="_blank">
                        <i class="zmdi zmdi-vimeo"></i>
                      </a>
                    </li>
                    <li>
                      <a href="//linkedin.com" target="_blank">
                        <i class="zmdi zmdi-linkedin-box"></i>
                      </a>
                    </li>
                    <li>
                      <a href="//skype.com" target="_blank">
                        <i class="zmdi zmdi-skype"></i>
                      </a>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
            <div class="col-lg-8">
              <!-- top bar right -->
              <div class="top-bar-right-wrapper">
                <router-link to="/Contact" class="ht-btn ht-btn--default d-inline-block">GET A QUOTE</router-link>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!--=======  End of header top bar  =======-->

      <!--=======  header info area  =======-->
      <div class="header-info-area">
        <div class="container">
          <div class="row align-items-center">
            <div class="col-lg-12">
              <div class="header-info-wrapper align-items-center">
                <!-- logo -->
                <div class="logo">
                  <router-link to="/">
                    <img src="assets/img/logo/logo.png" class="img-fluid" alt="Brand Logo" />
                  </router-link>
                </div>

                <!-- header contact info -->
                <div class="header-contact-info">
                  <div class="header-info-single-item">
                    <div class="header-info-single-item__icon">
                      <i class="zmdi zmdi-smartphone-android"></i>
                    </div>
                    <div class="header-info-single-item__content">
                      <h6 class="header-info-single-item__title">Phone</h6>
                      <p class="header-info-single-item__subtitle">
                        <a href="tel:0272551485">027 255 1485</a>
                      </p>
                    </div>
                  </div>
                  <div class="header-info-single-item">
                    <div class="header-info-single-item__icon">
                      <i class="zmdi zmdi-home"></i>
                    </div>
                    <div class="header-info-single-item__content">
                      <h6 class="header-info-single-item__title">Address</h6>
                      <p class="header-info-single-item__subtitle">Signal Hill Farm, Opoho</p>
                    </div>
                  </div>
                </div>

                <!-- mobile menu -->
                <div
                  class="mobile-navigation-icon"
                  id="mobile-menu-trigger"
                  @click="mobiletoggleClass('addClass', 'active')"
                >
                  <i></i>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!--=======  End of header info area =======-->

      <!--=======  header navigation area  =======-->
      <fixed-header>
        <div class="header-navigation-area default-bg">
          <div class="container">
            <div class="row">
              <div class="col-lg-12">
                <!-- header navigation -->
                <div class="header-navigation header-navigation--header-default position-relative">
                  <div class="header-navigation__nav position-static">
                    <nav>
                      <ul>
                        <li>
                          <router-link to="/">HOME</router-link>
                        </li>
                        <li>
                          <router-link to="/about">ABOUT</router-link>
                        </li>

                        <li>
                          <router-link to="/service">SERVICES</router-link>
                        </li>

                        <li>
                          <router-link to="/project">PROJECTS</router-link>
                        </li>
                        <li>
                          <router-link to="/contact">CONTACT</router-link>
                        </li>
                      </ul>
                    </nav>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </fixed-header>
      <!--=======  End of header navigation area =======-->
    </div>
  </div>
  <!--====================  End of header area  ====================-->
</template>

<script>
import FixedHeader from "vue-fixed-header";
export default {
  components: {
    FixedHeader
  },
  methods: {
    // offcanvas mobilemenu
    mobiletoggleClass(addRemoveClass, className) {
      const el = document.querySelector("#offcanvas-menu");
      if (addRemoveClass === "addClass") {
        el.classList.add(className);
      } else {
        el.classList.remove(className);
      }
    }
  }
};
</script>

<style lang="scss">
.vue-fixed-header--isFixed {
  left: 0;
  top: 0;
  width: 100vw;
  z-index: 999;
  position: fixed;
  box-shadow: 0 0 8px 1px rgba(0, 0, 0, 0.2);
  animation: 900ms cubic-bezier(0.2, 1, 0.22, 1) 0s normal none 1 running
    fadeInDown;
}
</style>