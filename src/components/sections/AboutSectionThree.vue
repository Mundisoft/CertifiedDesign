<template>
    <div class="about-section section-space--inner--120">
        <div class="container">
            <div class="row row-25 align-items-center">
                <div class="col-lg-6 col-12 mb-30">
                    <div class="about-image-two">
                        <img :src="data.aboutUs.image" alt="image">
                        <span class="video-popup">
                            <silentbox-single :src="data.youtubeLink">
                                <i class="ion-ios-play-outline"></i>
                            </silentbox-single>
                        </span>
                    </div>
                </div>
                <div class="col-lg-6 col-12 mb-30">
                    <div class="about-content-two">
                        <h3>{{ data.aboutUs.subTitle }}</h3>
                        <h1>{{ data.aboutUs.title }}</h1>
                        <h4>{{ data.aboutUs.shortDesc }}</h4>
                        <p>{{ data.aboutUs.desc }}</p>
                        <router-link to="service" class="ht-btn--default ht-btn--default--dark-hover section-space--top--20">Our Services</router-link>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import data from '../../data/about.json'
    export default {
        data () {
            return {
                data
            }
        }
    };
</script>