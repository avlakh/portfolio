<template>
    <SiteHeader></SiteHeader>
    <main>
        <HomeSection></HomeSection>
        <AboutMe ></AboutMe>
        <MyProjects></MyProjects>
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
import MyProjects from './components/MyProjects.vue';

export default {
    components: {
    SiteHeader,
    SiteFooter,
    HomeSection,
    AboutMe,
    MyCertificates,
    MyProjects
},
    
}

</script>

<style lang="scss">

@import '@/assets/css/norm.scss';
@import '@/assets/css/fonts.scss';
@import '@/assets/css/vars.scss';

</style>
