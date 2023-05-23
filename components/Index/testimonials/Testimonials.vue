<template>
    <section class="tvl-testimonials-section">
        <div class="tvl-testimonials-section-wrapper">
            <div id="tvl-testimonials-container" data-element-state="visible" class="tvl-testimonials-container">
                <h3 class="tvl-testimonials-container-heading">Testimonials</h3>
                <p class="tvl-testimonials-container-text">People love our work</p>
                <div class="tvl-testimonials-cards-container">
                    <template v-for="(testimonial, index) in testimonials">
                        <IndexTestimonialsTestimonialCards
                            :id="index"
                            :name=testimonial.name
                            :text=testimonial.text
                            :organisation=testimonial.organisation
                            :thumbnail=testimonial.thumbnail
                        />
                    </template>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    //import TestimonialCards from './TestimonialCards.vue';
    export default {
        name: 'Testimonials',
        data(){

            return {
                observer: null,
                testimonials: [
                    {
                        name:'Jhon Doe',
                        organisation: 'XYZ Org.',
                        thumbnail: 'mitesh_eps.jpg',
                        text: 'A truly Inspirational Event....It has been a great pleasure working with Liquid Media Live Events.'
                    },
                    {
                        name:'Jhon Doe',
                        organisation: 'XYZ Org.',
                        thumbnail: 'mitesh_eps.jpg',
                        text: 'A truly Inspirational Event....It has been a great pleasure working with Liquid Media Live Events.'
                    },
                    {
                        name:'Jhon Doe',
                        organisation: 'XYZ Org.',
                        thumbnail: 'mitesh_eps.jpg',
                        text: 'A truly Inspirational Event....It has been a great pleasure working with Liquid Media Live Events.'
                    },
                    {
                        name:'Jhon Doe',
                        organisation: 'XYZ Org.',
                        thumbnail: 'mitesh_eps.jpg',
                        text: 'A truly Inspirational Event....It has been a great pleasure working with Liquid Media Live Events.'
                    }
                ]
            }
        },
        methods: {

            initTestimonialObserver(){

                let options = this.$store.state.observerOptions ;
                this.observer = new IntersectionObserver(this.testimonialSectionAnimation, options) ;
            },

            testimonialSectionObserver(){

                if(!this.observer){

                    this.initTestimonialObserver() ;
                    this.observer.observe(document.getElementById('tvl-testimonials-container')) ;

                }
            },

            testimonialSectionAnimation(entries, observer){

                let target = entries[0].target,
                    isVisible = entries[0].isIntersecting ;

                    if(isVisible){

                        target.setAttribute('data-element-state', 'visible') ;
                        this.observer.unobserve(target) ;

                    }

            }
        },
        mounted(){

            //this.testimonialSectionObserver() ;
        }
    }
</script>

<style lang="scss">
    .tvl-testimonials-section{
        width: 100% ;
        height: auto ;
        padding: 0px 0px clamp(20px, 4vh, 40px) 0px ;
        position: relative ;
        z-index: 2;
        
        // &::before{
        //     content: "";
        //     width: 100% ;
        //     height: clamp(165px, 24vh, 240px) ;
        //     background-color: black;
        //     position: absolute;
        //     top: 0px;
        //     left: 0px ;
        //     z-index: -1;
        // }
    }
    .tvl-testimonials-section-wrapper{
        width: 100% ;
        display: flex ;
        flex-direction: column;
    }
    .tvl-testimonials-container{
        width: 90% ;
        min-width: 300px ;
        //max-width: 850px ;
        height: auto ;
        display: flex;
        flex-direction: column;
        padding: clamp(24px, 5vh, 32px) 0px ;
        align-self: center;
        background-color: #1C56BA;
        backdrop-filter: blur(50px);
        border-radius: 8px ;
        opacity: 0;
        transform: translateY(var(--scroll-y-offset));
        transition: var(--scroll-transition);

        &[data-element-state="visible"]{
            transform: translateY(0);
            opacity: 1;
        }
    }
    .tvl-testimonials-container-heading{
        font-size: 26px ;
        font-weight: 300 ;
        font-family: var(--font-family);
        text-align: center;
        padding-bottom: 6px ;
        color: white ;
    }
    .tvl-testimonials-container-text{
        width: fit-content;
        font-size: 12px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        text-align: center;
        align-self: center;
        padding: 4px 12px;
        margin-bottom: 8px;
        color: #1C56BA;
        border-radius: 20px ;
        background-color: white;
    }
    .tvl-testimonials-cards-container{
        width: 100% ;
        padding-top: clamp(24px, 8vh, 40px) ;
    }

    @media screen and (min-width:720px) {

        .tvl-testimonials-container{
            padding: clamp(32px, 10vh, 56px) 0px ;
        }
        .tvl-testimonials-container-heading{
            font-size: 35px ;
        }
        .tvl-testimonials-container-text{
            font-size: 14px ;
        }
    }

    @media screen and (min-width: 1024px ) {
        .tvl-testimonials-container{
            min-width: 850px ;
            border-radius: 16px ;
        }
        .tvl-testimonials-cards-container{
            width: 90% ;
            align-self: center;
        }
    }
</style>

