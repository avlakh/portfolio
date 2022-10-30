<template>
    <SiteHeader></SiteHeader>
    <main>

    </main>
    <SiteFooter></SiteFooter>
</template>

<script>

import SiteHeader from './components/SiteHeader.vue';
import SiteFooter from './components/SiteFooter.vue';

export default {
    components: {
        SiteHeader,
        SiteFooter
    }
}

</script>

<style>

@import '@/assets/css/norm.scss';
@import '@/assets/css/fonts.scss';
@import '@/assets/css/main.scss';

</style>
