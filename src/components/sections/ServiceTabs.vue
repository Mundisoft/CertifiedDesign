<template>
    <!--====================  service tab area ====================-->
    <div class="service-tab-area section-space--inner--120">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="section-title-area text-center">
                        <h2 class="section-title section-space--bottom--50">Our Services <span class="title-icon"></span></h2>
                    </div>
                </div>
                <div class="col-lg-12">
                    <!-- service tab wrapper -->
                    <div class="service-tab-wrapper">
                        <div class="row no-gutters">
                            <div class="col-md-4">
                                <div class="nav nav-tabs flex-column service-tab__link-wrapper">
                                    <a class="nav-item nav-link " @click.prevent="setActive('home')" :class="{ active: isActive('home') }" href="#home"> <span class="icon"><i class="flaticon-002-welding"></i></span> <span class="text">Heavy Vehicles</span></a>
                                    <a class="nav-item nav-link" @click.prevent="setActive('profile')" :class="{ active: isActive('profile') }" href="#profile"> <span class="icon"><i class="flaticon-004-walkie-talkie"></i></span> <span class="text">Plant Design</span></a>
                                    <a class="nav-item nav-link" @click.prevent="setActive('about')" :class="{ active: isActive('about') }" href="#about"> <span class="icon"><i class="flaticon-015-cart"></i></span> <span class="text">Machine Design</span></a>
                                    <a class="nav-item nav-link" @click.prevent="setActive('contact')" :class="{ active: isActive('contact') }" href="#contact"> <span class="icon"><i class="flaticon-010-tank-1"></i></span> <span class="text">Certification</span></a>
                                </div>
                            </div>
                            <div class="col-md-8">
                                <div class="tab-content service-tab__content-wrapper">
                                    <div class="tab-pane fade" :class="{ 'active show': isActive('home') }" id="home">
                                        <div class="service-tab__single-content-wrapper bg-img" :style="{'background-image':'url(assets/img/backgrounds/service-tab1.jpg)'}">
                                            <div class="service-tab__single-content">
                                                <h3 class="service-tab__title">Heavy Vehicles</h3>
                                                <p class="service-tab__text">Heavy Vehicle design and certification from bent tow eye replacement to specialist trailer design.</p>
                                                <router-link to="/service-details" class="see-more-link">Read More</router-link>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="tab-pane fade" :class="{ 'active show': isActive('profile') }" id="profile">
                                        <div class="service-tab__single-content-wrapper bg-img" :style="{'background-image':'url(assets/img/backgrounds/service-tab1.jpg)'}">
                                            <div class="service-tab__single-content">
                                                <h3 class="service-tab__title">Plant Design</h3>
                                                <p class="service-tab__text">Plant design and certification from lifting beams to shop trestles.</p>
                                                <router-link to="/service-details" class="see-more-link">Read More</router-link>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="tab-pane fade" :class="{ 'active show': isActive('about') }" id="about">
                                        <div class="service-tab__single-content-wrapper bg-img" :style="{'background-image':'url(assets/img/backgrounds/service-tab1.jpg)'}">
                                            <div class="service-tab__single-content">
                                                <h3 class="service-tab__title">Machine Design</h3>
                                                <p class="service-tab__text">Machine design from conveyors to production line machinery.</p>
                                                <router-link to="/service-details" class="see-more-link">Read More</router-link>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="tab-pane fade" :class="{ 'active show': isActive('contact') }" id="contact">
                                        <div class="service-tab__single-content-wrapper bg-img" :style="{'background-image':'url(assets/img/backgrounds/service-tab1.jpg)'}">
                                            <div class="service-tab__single-content">
                                                <h3 class="service-tab__title">Certification</h3>
                                                <p class="service-tab__text">Certified Engineer, ready to take on your certification and design needs.</p>
                                                <router-link to="/service-details" class="see-more-link">Read More</router-link>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!--====================  End of service tab area  ====================-->
</template>

<script>
    export default {
        data(){
            return {
                activeItem: 'home'
            }
        },
        methods: {
            isActive (menuItem) {
                return this.activeItem === menuItem
            },
            setActive (menuItem) {
                this.activeItem = menuItem
            }
        }
    };
</script>