<template>
    <div class="hero-content-container">
        <div class="hero-content-wrapper">
            <div data-hero-content-row="main" class="hero-content-wrapper-rows">
                <HeroContentMain />
            </div>
            <div data-hero-content-row="about" class="hero-content-wrapper-rows">
                <HeroContentAbout />
            </div>
        </div>
    </div>
</template>

<script>
import HeroContentAbout from './HeroContentAbout.vue';
import HeroContentMain from './HeroContentMain.vue';

    export default {
    name: "HeroContent",
    components: { HeroContentMain, HeroContentAbout }
}
</script>

<style lang="scss">
    .hero-content-container{
        width: 100% ;
        display: flex ;
        flex-direction: column;
        padding-top: clamp(80px, 20vh, 120px);
        background-image: linear-gradient(to bottom, rgba(255, 255, 255, 0), rgba(255, 255, 255, 0.3)),
                            linear-gradient(to right, rgba(255, 255, 255, 0), rgba(255, 255, 255, 1));
    }
    .hero-content-wrapper{
        width: 90% ;
        min-width: 290px ;
        align-self: center;
        display: flex ;
        flex-direction: column;
    }
    .hero-content-wrapper-rows{
        width: 100% ;
        align-self: center;
        display: flex ;
        flex-direction: column;
        padding-bottom: 40px ;
    }

    @media screen and (min-width: 720px) {
        .hero-content-wrapper{
            flex-direction: row;
        }
        .hero-content-wrapper-rows{
            width: unset;

            &[data-hero-content-row='main']{
                flex: 1;
                padding-right: 15px ;
                box-sizing: border-box;
                
            }

            &[data-hero-content-row='about']{
                width: 35% ;
                min-width: 300px ;
            }
        }
    }
</style>