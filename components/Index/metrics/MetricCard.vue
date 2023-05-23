<template>
    <div :id="`${id}-metric-card`" class="home-page-metrics-card">
        <p class="home-page-metrics-title">{{ title }}</p>
        <p class="home-page-metrics-number">{{ number }}+</p>
    </div>
</template>

<script>
    export default {
        name: 'MetricCard',
        props: {
            title: String,
            num: Number,
            id: String
        },
        data(){

            return {
                observer: null,
                number: 0
            }
        },
        methods: {

            increments(){

                if(this.number < this.$props.num){

                    setTimeout(() => {
                        this.number += Math.round(this.$props.num/20) ;
                        return this.increments() ;
                    }, 75);

                }else {
                    return false ;
                }
            },

            metricCardObserver(){

                if(!this.observer){

                    let target = document.getElementById(`${this.$props.id}-metric-card`) ;
                    this.observer = new IntersectionObserver(this.metricCardAnimation, {
                                        root: null,
                                        rootMargin: '0px',
                                        threshold: 1.0
                                    }) ;

                    this.observer.observe(target) ;
                }
            },

            metricCardAnimation(entries, observer){

                let entry = entries[0] ;

                    if(entry.isIntersecting){

                        this.increments() ;
                        this.observer.unobserve(entry.target) ;
                    }
            }

        },

        mounted(){
            this.metricCardObserver() ;
        }
    }
</script>

<style lang="scss">
    .home-page-metrics-card{
        width: 150px;
        align-self: center;
        display: flex ;
        flex-direction: column;
        padding: 16px 0px 32px 0px ;
    }
    .home-page-metrics-title{
        width: 95px ;
        font-size: 15px ;
        font-family: var(--font-family) ;
        font-weight: 400;
        text-align: center;
        align-self: center;
        color: #1D5982;
        line-height: 1.45;
        padding-bottom: 16px ;
    }
    .home-page-metrics-number{
        font-size: 35px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        text-align: center;
    }

    @media screen and (min-width:720px) {
        .home-page-metrics-title{
            width: 105px ;
            font-size: 17px ;
        }
        .home-page-metrics-number{
            font-size: 45px ;
        }
    }
</style>