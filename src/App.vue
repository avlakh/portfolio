<template>
    <SiteHeader></SiteHeader>
    <main>
        <HomeSection></HomeSection>
        <AboutMe></AboutMe>
    </main>
    <SiteFooter></SiteFooter>
</template>

<script>

import SiteHeader from '@/components/SiteHeader.vue';
import SiteFooter from '@/components/SiteFooter.vue';
import HomeSection from '@/components/HomeSection.vue';
import AboutMe from '@/components/AboutMe.vue';

export default {
    components: {
        SiteHeader,
        SiteFooter,
        HomeSection,
        AboutMe
    }
}

</script>

<style lang="scss">

@import '@/assets/css/norm.scss';
@import '@/assets/css/fonts.scss';

</style>
