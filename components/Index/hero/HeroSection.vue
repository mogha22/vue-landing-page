<template>
    <section class="home-page-hero-section">
        <div class="home-page-hero-section-wrapper">
            <div data-hero-wrapper-row="background" class="home-page-hero-wrapper-rows"></div>
            <div data-hero-wrapper-row="content" class="home-page-hero-wrapper-rows">
                <HeroContent />
            </div>
        </div>
    </section>
</template>

<script>
    import HeroContent from './HeroContent.vue';

    export default {
        name: "HeroSection",
        components: { HeroContent }
    }
</script>

<style lang="scss">
    .home-page-hero-section{
        width: 100% ;
        height: auto ;
    }
    .home-page-hero-section-wrapper{
        width: 100% ;
        height: auto ;
        display: grid ;
        grid-template-columns: 1fr ;
        grid-template-rows: 1fr ;
    }
    .home-page-hero-wrapper-rows{
        grid-column: 1/2 ;
        grid-row: 1/2 ;

        &[data-hero-wrapper-row="background"]{
            background-image: url('~/assets/images/home/hero/hero-background-1.jpg'),
                                linear-gradient(to right, rgba(255, 255, 255, 0), rgba(255, 255, 255, 1)),
                                linear-gradient(to bottom, rgba(255, 255, 255, 0), rgba(255, 255, 255, 1));
            background-position: 30% center;
            background-size: cover;
            background-blend-mode: lighten;
        }

    }
</style>