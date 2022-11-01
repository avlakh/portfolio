<template>
    <section id="about">
        <div class="container">
            <div class="content-container">
                <div class="about-me-flex">
                    <div class="about-me-img">
                        <img src="@/assets/images/main-photo.jpg" alt="main photo">
                    </div>
                    <div class="about-me-text">
                        <h2>About Me</h2>
                        <h3>Artem Vlakh</h3>
                        <h4>Front-end Developer</h4>
                        <h5><span class="bolder-span">Residence:</span>Poland</h5>
                        <h5><span class="bolder-span">City:</span>Warsaw</h5>
                        <h5><span class="bolder-span">Age:</span>26</h5>
                        <p>Hey &#128075; My name is Artem and I'm just beginning my journey in Front-end Development. Currently expanding my skillset within web development and looking for job opportunities.</p>
                        <p>An open-minded, result-oriented specialist with great time-management skills that strives to learn more.</p>
                        <div class="about-me-skills">
                            <span>HTML5</span><span>CSS3/SCSS</span><span>JavaScript</span><span>Vue3</span><span>AJAX</span><span>Flex/Grid</span><span>Bootstrap5</span><span>jQuery</span><span>GIT/Github</span><span>APIs</span><span>Figma</span><span>RWD/AWD</span>
                        </div>
                        <a href="#" class="cv-btn"><span>Download CV</span><span class=""><i class="icon icon-file_download"></i></span></a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'AboutMe'
}
</script>

<style lang="scss">

@import '@/assets/css/vars.scss';

#about {
    scroll-margin-top: 60px;
    height: 2000px;
    // TODO: change when aboutme is done
}

.content-container {
    padding: 25px 0;
}

.about-me-flex {
    display: flex;
    gap: 40px;
}

.about-me-img {
    border-radius: 12px;
    width: 60%;
    overflow: hidden;
    aspect-ratio: 1 / 1;
    /* border: 10px solid lightgrey; */
    box-shadow: 10px 10px 10px #d1d9e6, -10px -10px 10px #f9f9f9;
    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: 0% 40%;
    }
}
.about-me-text {
    h2 {
        font-size: 32px;
        line-height: 42px;
        position: relative;
        margin-bottom: 20px;
    }
    h3 {
        font-size: 22px;
        line-height: 26px;
    }
    h4 {
        font-size: 18px;
        line-height: 26px;
        margin-bottom: 16px;
        position: relative;
        color: $accent-clr;
        &:before {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 26%;
            border: 1px solid $secondary-clr;
        }
    }
    p {
        padding-right: 20%;
        margin-bottom: 10px;
        &:last-of-type {
            margin-bottom: 30px;
        }
    }
    h5 {
        font-size: 18px;
        line-height: 22px;
        margin-bottom: 8px;
        font-weight: 400;
        &:last-of-type {
            margin-bottom: 30px;
        }
    }
}

.bolder-span {
    font-weight: 700;
    margin-right: 8px;
}

.about-me-skills {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    margin-bottom: 20px;
    span {
        padding: 5px 20px;
        border-radius: 12px;
        background-color: #e8ebf0;
        box-shadow: 10px 10px 10px #d1d9e6, -10px -10px 10px #f9f9f9;
        color: $accent-clr;
    }
}

.cv-btn {
    display: block;
    padding: 10px 50px;
    background-color: #e8ebf0;
    border-radius: 12px;
    width: 30%;
    box-shadow: 10px 10px 10px #d1d9e6, -10px -10px 10px #f9f9f9;
    text-align: center;
    color: inherit;
    &:hover {
        color: $accent-clr;
    }
    &:active {
        box-shadow: inset 5px 5px 5px #d1d9e6, inset -5px -5px 5px #f9f9f9;
    }
    span:first-of-type {
        margin-right: 10px;
    }
    i {
        font-size: 20px;
        position: relative;
        &:before {
            position: absolute;
            top: 3px;
        }
    }
}

</style>