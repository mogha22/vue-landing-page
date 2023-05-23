<template>
    <div class="home-page-test-content-container">
        <div class="home-page-text-content-wrapper">
            <h3 class="home-page-test-content-heading">Latest Tests Available</h3>
            <p class="home-page-test-content-text">We have in-house lab facility to give our patients a seamless and hassle free experience of getting their Class 2 medical examination conducted.</p>
            <div class="home-page-test-list-container">
                <p v-for="test in tests" class="home-page-test-list"><span class="material-symbols-outlined">check_circle</span> {{ test }}</p>
            </div>
            <p class="home-page-test-content-disclaimer">Note : ENT Tests not included</p>
        </div>
        <div class="home-page-test-button-container">
            <Button type="light" />
        </div>
    </div>
</template>

<script>
    export default {
        name: 'TestContent',
        data(){

            return {
                tests: [
                            'Radiograph Chest PA view', 
                            'Lipid Profile', 
                            'Thyroid Function test (T3, T4 & TSH)',
                            'Liver Function Test',
                            'Kidney Function Test',
                            'Ultrasoundgraphy Abdomen & Pelvis'
                        ]
            }
        }
    }
</script>

<style lang="scss">
    .home-page-test-content-container{
        width: 90% ;
        max-width: 400px ;
        height: 100% ;
        align-self: center;
        display: flex ;
        flex-direction: column;
    }
    .home-page-test-content-wrapper{
        width: 100% ;
        flex: 2;
        display: flex ;
        flex-direction: column;
    }
    .home-page-test-content-heading{
        font-size: 30px ;
        font-weight: 300 ;
        font-family: var(--font-family);
        text-align: left;
        color: white ;
        padding-bottom: 24px ;
    }
    .home-page-test-content-text{
        font-size: 14px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        text-align: left;
        color: white ;
        line-height: 1.5;
    }
    .home-page-test-list-container{
        width: 100% ;
        padding: 16px 0px ;
        padding-bottom: 40px ;
    }
    .home-page-test-list{
        font-size: 12px ;
        font-weight: 500 ;
        font-family: var(--font-family);
        color: white ;
        display: inline-block;
        padding: 3px 9px 3px 0px ;
        margin: 4px 0px ; 

        .material-symbols-outlined{
            font-size: 15px ;
            color: #24FF00 ;
            transform: translateY(-1px);
        }

        span{
            display: inline-block ;
            vertical-align: middle;
        }
    }
    .home-page-test-content-disclaimer{
        font-size: 12px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        color: white ;
        padding: 8px 0px ;
    }
    .home-page-test-button-container{
        width: 100% ;
        padding-top: 35px ;
    }

    @media screen and (min-width:540px) {
        .home-page-test-content-heading{
            font-size: 42px ;
            padding-bottom: 32px ;
        }
        .home-page-test-content-text{
            font-size: 16px ;
            font-weight: 300 ;
        }
        .home-page-test-content-disclaimer{
            font-size: 14px ;
        }
    }

    @media screen and (min-width: 1024px) {
        .home-page-test-content-container{
            max-width: 480px ;
        }
        .home-page-test-content-heading{
            font-size: 51px ;
            font-weight: 200;
        }
        .home-page-test-content-text{
            font-size: 17px ;
        }
        .home-page-test-content-disclaimer{
            font-size: 13px ;
        }
    }
</style>