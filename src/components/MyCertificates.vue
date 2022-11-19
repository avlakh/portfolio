<template>
    <section id="certificates">
        <div class="container">
            <h2>Certificates</h2>
            <div class="certificates-grid">
                <div class="card-img">
                    <a href="https://lms.beetroot.academy/diploma/ckyjz27d0sgnq0824288qos59" target="_blank">
                        <img src="@/assets/images/certificates/beetroot-certificate.jpg" alt="Beetroot Certificate">
                    </a>
                </div>
                <div class="card-img">
                    <a href="https://www.freecodecamp.org/certification/fcc608e09ce-8042-4f7d-bdfc-ce97e48ee189/javascript-algorithms-and-data-structures" target="_blank">
                        <img src="@/assets/images/certificates/freecodecamp_js.jpg" alt="Free Code Camp JS">
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
    h2 {
        margin-bottom: 40px;
    }
}

.certificates-grid {
    display: grid;
    grid-template: repeat(auto-fit, minmax(200px, 1fr)) / repeat(auto-fit, minmax(300px, 1fr));
    gap: 40px;
    .card-img {
        width: 100%;
        height: 100%;
        border: 10px solid $secondary-clr;
        border-radius: 12px;
        box-shadow: 10px 10px 10px #d1d9e6, -10px -10px 10px #f9f9f9;
        transition: all 0.2s ease;
        &:hover {
            transform: scale(1.1);
        }
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
}


</style>