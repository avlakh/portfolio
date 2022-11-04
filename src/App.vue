<template>
    <SiteHeader></SiteHeader>
    <main>
        <HomeSection></HomeSection>
        <AboutMe></AboutMe>
        <section id="projects">
            <div class="container">
                <h2>Projects</h2>
                <Carousel :settings="sliderSettings">
                    <Slide v-for="slide in slides" :key="slide">
                        <div class="content-wrap">
                            <div class="img-wrap">
                                <img :src="require('@/assets/images/projects/'+ slide.img)" :alt="slide.imgAlt">
                            </div>
                            <p>{{slide.descr}}</p>
                            <a :href="slide.url" target="_blank"></a>
                        </div>
                    </Slide>
                    <template #addons>
                        <Navigation />
                    </template>
                </Carousel>
            </div>
        </section>
        <MyCertificates></MyCertificates>
    </main>
    <SiteFooter></SiteFooter>
</template>

<script>

import SiteHeader from '@/components/SiteHeader.vue';
import SiteFooter from '@/components/SiteFooter.vue';
import HomeSection from '@/components/HomeSection.vue';
import AboutMe from '@/components/AboutMe.vue';
import MyCertificates from '@/components/MyCertificates.vue';
import axios from 'axios';
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Navigation } from 'vue3-carousel'

export default {
    components: {
    SiteHeader,
    SiteFooter,
    HomeSection,
    AboutMe,
    Carousel,
    Slide,
    Navigation,
    MyCertificates
},
    data(){
        return {
            slides: [],
            sliderSettings: {
                itemsToShow: 1.1,
                autoplay: 3000,
				wrapAround: true
            }
        }
    },
    created(){
        axios
            .get('data/MyProjects.json')
            .then(resp =>{
                this.slides = resp.data;
                console.log(this.slides);
            });
    }
}

</script>

<style lang="scss">

@import '@/assets/css/norm.scss';
@import '@/assets/css/fonts.scss';
@import '@/assets/css/vars.scss';
@import '@/assets/css/main.scss';


</style>
