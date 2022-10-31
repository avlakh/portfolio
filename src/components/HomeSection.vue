<template>
    <section class="home-section">
        <div class="container">
            <div class="content-container">
                <div class="home-section-text">
                    <h1>Artem Vlakh</h1>
                    <h4>Front End Developer</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Distinctio ipsam esse autem voluptate maiores architecto, officiis optio quibusdam odio eum!</p>
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
    background-color: #e9f1fb;
    padding: 80px 0;
    .container {
        box-shadow: inset 10px 10px 10px #d1d9e6, inset -10px -10px 10px #f9f9f9;
        border-radius: 12px;
        .content-container {
            width: 90%;
            height: 100%;
            max-width: 1200px;
            margin: 0 auto;
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
        font-size: 50px;
        line-height: 60px;
        background: linear-gradient(90deg, #026ee2, #013369);
        color: transparent;
        -webkit-background-clip: text;
    }
    h4 {
        font-size: 26px;
        line-height: 32px;
        margin-bottom: 16px;
    }
    p {
        padding-right: 20%;
        margin-bottom: 30px;
    }
    .btn {
        display: inline-block;
        text-transform: capitalize;
        width: 30%;
        height: 100%;
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