<template>
    <section class="home-section">
        <div class="container">
            <div class="content-container">
                <div class="home-section-text">
                    <h1>Artem Vlakh</h1>
                    <h2>Front-end Developer</h2>
                    <a href="#about" class="btn">About me</a>
                </div>
                <div class="home-section-img">
                    <img src="@/assets/images/main-photo.jpg" alt="main photo">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'HomeSection'
}
</script>

<style lang="scss">

@import '@/assets/css/vars.scss';

.home-section {
    height: 100vh;
    padding: 80px 0;
    .container {
        box-shadow: inset 10px 10px 10px #d1d9e6, inset -10px -10px 10px #f9f9f9;
        border-radius: 12px;
        .content-container {
            display: flex;
            align-items: center;
            justify-content: start;
            padding: 25px 0;
        }
    }
}

.home-section-text {
    width: 50%;
    h1 {
        font-size: 64px;
        line-height: 72px;
        background: linear-gradient(to bottom, #026ee2 30%, #0355ad 70%);
        color: transparent;
        -webkit-background-clip: text;
        margin-bottom: 15px;
    }
    h2 {
        font-size: 26px;
        line-height: 32px;
        margin-bottom: 32px;
    }
    .btn {
        display: inline-block;
        text-transform: capitalize;
        width: 30%;
        padding: 10px 20px;
        transition: all 0.2s ease;
        border-radius: 12px;
        background: $btn-clr;
        text-align: center;
        font-size: 20px;
        box-shadow: 5px 5px 5px #d1d9e6, -5px -5px 5px #f9f9f9;
        &:hover {
            color: $accent-clr;
        }
        &:active {
            box-shadow: inset 5px 5px 5px #d1d9e6, inset -5px -5px 5px #f9f9f9;
        }
    }
}

.home-section-img {
    width: 50%;
    height: 100%;
    border-radius: 12px;
    overflow: hidden;
    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
}

</style>