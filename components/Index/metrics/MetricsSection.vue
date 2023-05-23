<template>
    <div class="home-page-metrics-section">
        <div class="home-page-metrics-section-wrapper">
            <div v-for="(metric, key) in metrics" class="home-page-metrics-rows">
                <MetricCard
                    :title="metric.title"
                    :num="metric.num"
                    :id="key"
                />
            </div>
        </div>
    </div>
</template>

<script>
    import MetricCard from './MetricCard.vue';
    export default {
        name: 'MetricsSection',
        components: {MetricCard},
        data(){
            return {

                metrics :{
                            experience: {
                                            title: 'Years of Experience',
                                            num: 12
                                        },

                            medicals: {
                                            title: 'Medicals Done',
                                            num: 200
                                        },

                            patients: {
                                            title: 'Patients Served',
                                            num: 5000
                                        },
                        }
            }
        }
    }
</script>

<style lang="scss">
    .home-page-metrics-section{
        width: 100% ;
        display: flex ;
        flex-direction: column;
        margin: clamp(60px, 12vh, 120px) 0px clamp(30px, 6vh, 60px) 0px ;
    }
    .home-page-metrics-section-wrapper{
        width: 90% ;
        max-width: 600px ;
        align-self: center;
        display: flex ;
        flex-direction: column;
        padding: 15px 0px ;
    }
    .home-page-metrics-rows{
        width: 100% ;
        align-self: center;
        display: flex;
        flex-direction: column;
    }

    @media screen and (min-width: 540px) {
        .home-page-metrics-section-wrapper{
            flex-direction: row;
            justify-content: space-around;
        }
        .home-page-metrics-rows{
            width: 30% ;
            align-self: center;
        }
        
    }
</style>