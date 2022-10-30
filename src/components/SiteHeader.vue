<template>
    <!-- TODO: side block & page overlay to be done  -->
    <!-- TODO: mobile menu to be done -->
    <header>
        <div class="container">
            <nav id="main-menu">
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#about">About me</a></li>
                    <li><a href="#stack">Skills</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>
    <!-- SECTIONS:
        1. HOME
        2. STACK OF TECHNOLOGIES
        3. ABOUT ME
        4. MY PROJECTS
        5. CONTACT
    -->
</template>

<script>
    export default {
        name: 'SiteHeader',
    }
</script>

<style lang="scss">
    @import '@/assets/css/header.scss';
</style>