<template>
    <section id="certificates">
        <div class="container">
            <h2>Certificates</h2>
            <div class="certificates-flex">
                <div class="card-img">
                    <a href="https://lms.beetroot.academy/diploma/ckyjz27d0sgnq0824288qos59" target="_blank">
                        <img src="@/assets/images/certificates/beetroot-certificate.jpg" alt="Beetroot Certificate">
                    </a>
                </div>
                <div class="card-img">
                    <a href="https://udemy-certificate.s3.amazonaws.com/pdf/UC-a66a0dc3-91b8-4918-88bb-bf57a2d6ff46.pdf" target="_blank">
                        <img src="@/assets/images/certificates/udemy-react.jpg" alt="Udemy React Project">
                    </a>
                </div>
                <div class="card-img">
                    <a href="https://www.freecodecamp.org/certification/fcc608e09ce-8042-4f7d-bdfc-ce97e48ee189/javascript-algorithms-and-data-structures" target="_blank">
                        <img src="@/assets/images/certificates/freecodecamp_js.jpg" alt="Free Code Camp JS">
                    </a>
                </div>
                <div class="card-img">
                    <a href="https://www.freecodecamp.org/certification/fcc608e09ce-8042-4f7d-bdfc-ce97e48ee189/responsive-web-design" target="_blank">
                        <img src="@/assets/images/certificates/freecodecamp_rwd.jpg" alt="Free Code Camp RWD">
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MyCertificates',
}
</script>

<style lang="scss">

@import '@/assets/css/vars.scss';

#certificates {
    padding: 40px 0;
    scroll-margin-top: 30px;
    h2 {
        margin-bottom: 40px;
    }
}

.certificates-flex {
    display: flex;
    flex-wrap: wrap;
    flex: 1;
    gap: 40px;
    .card-img {
        flex: 35%;
        border: 10px solid $secondary-clr;
        border-radius: 12px;
        box-shadow: 10px 10px 10px #d1d9e6, -10px -10px 10px #f9f9f9;
        transition: all 0.2s ease;  
        &:hover {
            transform: scale(1.05);
        }
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
}

@media screen and (max-width: 750px) {
    #certificates {
        padding: 20px 0;
    }
}

@media screen and (max-width: 500px) {
    .certificates-flex .card-img {
        flex: 50%;
        &:hover {
            transform: none;
        }
    }
    
    
}

</style>