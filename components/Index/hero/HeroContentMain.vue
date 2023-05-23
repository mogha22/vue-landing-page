<template>
    <div class="hero-content-main">
        <h1 class="hero-content-heading">Get your Aviation Class II Medical Done in Delhi, NCR</h1>
        <p class="hero-content-text">The most trusted and reliable place in Delhi, NCR to get medically certified.</p>
        <div class="hero-content-list-container">
            <p v-for="feature in features" class="hero-content-list-text"><span class="material-symbols-outlined">priority</span> <span class="hero-content-list-span">{{ feature }}</span></p>
        </div>
        <div class="hero-trusted-by-container">
            <p class="hero-trusted-by-text">Trusted by 200+ Patients</p>
            <div class="hero-trusted-by-images">
                <img data-trusted-image="one" src="~/assets/images/home/hero/trusted-by/image-1.png" alt="image" class="hero-trusted-by-image hero-trusted-by-image-1">
                <img data-trusted-image="2" src="~/assets/images/home/hero/trusted-by/image-2.png" alt="image" class="hero-trusted-by-image hero-trusted-by-image-2">
                <img data-trusted-image="3" src="~/assets/images/home/hero/trusted-by/image-3.png" alt="image" class="hero-trusted-by-image hero-trusted-by-image-3">
                <img data-trusted-image="4" src="~/assets/images/home/hero/trusted-by/image-4.png" alt="image" class="hero-trusted-by-image hero-trusted-by-image-4">
                <img data-trusted-image="5" src="~/assets/images/home/hero/trusted-by/image-5.png" alt="image" class="hero-trusted-by-image hero-trusted-by-image-5">
                <img data-trusted-image="6" src="~/assets/images/home/hero/trusted-by/image-6.png" alt="image" class="hero-trusted-by-image hero-trusted-by-image-6">
            </div>
        </div>
        <Button type="dark" />
    </div>
</template>

<script>
    export default {
        name: 'HeroContentMain',
        data(){

            return {
                features: [
                            'Class 2 Medical',
                            'DGCA Certified',
                            'Lab Facility',
                            'Same Day Report'
                        ]
            }
        }
    }
</script>

<style lang="scss">
    .hero-content-main{
        width: 100% ;
        align-self: center;
        padding: clamp(40px, 10vh, 60px) 0px;
    }
    .hero-content-heading{
        font-size: 32px ;
        font-weight: 900 ;
        font-family: var(--font-family);
        color: #1D2124 ;
        padding-bottom: 32px ;
    }
    .hero-content-text{
        font-size: 15px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        color: #1D2124 ;
        line-height: 1.45;
    }
    .hero-content-list-container{
        width: 100% ;
        padding-top: 40px ;
    }
    .hero-content-list-text{
        font-size: 12px ;
        font-weight: 700 ;
        font-family: var(--font-family);
        color: #1D2124 ;
        padding: 4px 10px 4px 0px ;
        display: inline-block;

        .material-symbols-outlined{
            font-size: 18px ;
            color: #269200 ;
        }
        span{
            display: inline-block;
            vertical-align: middle ;
        }
    }
    .hero-trusted-by-container{
        width: 100% ;
        margin-top: 48px ;
        margin-bottom: 32px;
    }
    .hero-trusted-by-text{
        font-size: 11px ;
        font-weight: 600 ;
        font-family: var(--font-family);
        color: black ;
        padding-bottom: 8px ;
    }
    .hero-trusted-by-images{
        width: 100% ;
    }
    .hero-trusted-by-image{
        width: 40px ;
        height: auto ;

        &[data-trusted-image="1"]{
            transform: translateX(-10px);
        }

        &[data-trusted-image="2"]{
            transform: translateX(-15px);
        }
        &[data-trusted-image="3"]{
            transform: translateX(-30px);
        }
        &[data-trusted-image="4"]{
            transform: translateX(-45px);
        }
        &[data-trusted-image="5"]{
            transform: translateX(-60px);
        }
        &[data-trusted-image="6"]{
            transform: translateX(-75px);
        }
    }

    @media screen and (min-width: 1024px) {
        .hero-content-heading{
            font-size: 52px ;
        }
        .hero-content-text{
            font-size: 18px ;
        }
        .hero-content-list-text{
            font-size: 13px ;
            font-weight: 600 ;
            padding: 4px 20px 4px 0px ;

        }
    }
</style>