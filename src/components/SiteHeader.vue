<template>
    <div id="side-block" :class="{'open': isMobileMenuOpened}">
        <div id="mobile-side-menu">
            <ul>
                <li><a href="#" @click="toggleMobileMenu"><span class="nav-link">Home</span></a></li>
                <li><a href="#about" @click="toggleMobileMenu"><span class="nav-link">About me</span></a></li>
                <li><a href="#projects" @click="toggleMobileMenu"><span class="nav-link">Projects</span></a></li>
                <li><a href="#certificates" @click="toggleMobileMenu"><span class="nav-link">Certificates</span></a></li>
                <li><a href="#contact" @click="toggleMobileMenu"><span class="nav-link">Contact</span></a></li>
                <li><button class="hamburger hamburger--spin" type="button" :class="{'is-active' : isMobileMenuOpened}" @click="toggleMobileMenu"><span class="hamburger-box"><span class="hamburger-inner"></span></span></button></li>
            </ul>
        </div>
    </div>
    <div id="page-overlay" :class="{'open': isMobileMenuOpened}" @click="toggleMobileMenu"></div>
    <header :class="{'header-scroll' : scrollPosition > 30}">
        <div class="container">
            <nav id="main-menu">
                <ul>
                    <li><a href="#"><span class="nav-link">Home</span></a></li>
                    <li><a href="#about"><span class="nav-link">About me</span></a></li>
                    <li><a href="#projects"><span class="nav-link">Projects</span></a></li>
                    <li><a href="#certificates"><span class="nav-link">Certificates</span></a></li>
                    <li><a href="#contact"><span class="nav-link">Contact</span></a></li>
                </ul>
            </nav>
            <div id="mobile-main-menu">
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><button class="hamburger hamburger--spin" type="button" :class="{'is-active' : isMobileMenuOpened}" @click="toggleMobileMenu">
                    <span class="hamburger-box"><span class="hamburger-inner"></span></span></button></li>
                </ul>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'SiteHeader',
    data () {
        return {
            scrollPosition: null,
            isMobileMenuOpened: false
        }
    },
    mounted() {
        window.addEventListener('scroll', this.updateScroll);
        window.addEventListener('resize', this.updateScroll);
    },
    methods: {
        updateScroll() {
            if (window.innerWidth >= 750){
                this.scrollPosition = window.scrollY;
            }
        },
        toggleMobileMenu(){
			this.isMobileMenuOpened = !this.isMobileMenuOpened;
			document.querySelector('body').classList.toggle('hidden')
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