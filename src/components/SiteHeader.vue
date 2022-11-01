<template>
    <!-- TODO: side block & page overlay to be done  -->
    <!-- TODO: mobile menu to be done -->
    <header :class="{'header-scroll' : scrollPosition > 30}">
        <div class="container">
            <nav id="main-menu">
                <ul>
                    <li><a href="#"><span class="nav-link">Home</span></a></li>
                    <li><a href="#about"><span class="nav-link">About me</span></a></li>
                    <li><a href="#projects"><span class="nav-link">Projects</span></a></li>
                    <li><a href="#certifications"><span class="nav-link">Certifications</span></a></li>
                    <li><a href="#contact"><span class="nav-link">Contact</span></a></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    name: 'SiteHeader',
    data () {
        return {
            scrollPosition: null
        }
    },
    mounted() {
        window.addEventListener('scroll', this.updateScroll);
    },
    methods: {
        updateScroll() {
            this.scrollPosition = window.scrollY;
        }
    },
    destroy() {
        window.removeEventListener('scroll', this.updateScroll)
    }
}
</script>

<style lang="scss">
@import '@/assets/css/header.scss';
</style>