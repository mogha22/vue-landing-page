<template>
    <section id="tests" class="home-page-tests-section">
        <div class="home-page-tests-section-wrapper">
            <div data-test-row="image" class="home-page-test-rows">
                <div class="home-page-test-image-container">
                    <img data-test-image="forward" src="~/assets/images/home/tests/image-1.jpg" alt="" class="home-page-test-image">
                </div>
            </div>
            <div data-test-row="content" class="home-page-test-rows">
                <IndexTestsTestContent />
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'Tests'
    }
</script>

<style lang="scss">
    .home-page-tests-section{
        width: 100% ;
        background-color: #2A7FBA;
        display: flex ;
        flex-direction: column ;
    }
    .home-page-tests-section-wrapper{
        width: 90% ;
        align-self: center;
        padding: clamp(30px, 15vh, 50px);
        display: flex ;
        flex-direction: column-reverse;
    }
    .home-page-test-rows{
        width: 100% ;
        align-self: center;
        display: flex ;
        flex-direction: column;
        padding: clamp(35px, 10vh, 55px) 0px ;
    }
    .home-page-test-image-container{
        width: 75% ;
        max-width: 320px ;
        align-self: center;
        height: auto ;
        display: flex ;
        flex-direction: column;
        position: relative;
        z-index: 2;

        &::before{
            content: '';
            width: 100% ;
            height: 100% ;
            position: absolute;
            top: 0px ;
            left: 0px ;
            background-image: url('~/assets/images/home/tests/image-2.jpg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            transform: translate(-12.5%, -30px);
            z-index: -1;
        }
    }
    .home-page-test-image{
        width: 100% ;
        height: auto ;
        align-self: center;
        transform: translate(12.5%, 30px);
        position: relative;
        z-index: 2;
    }

    @media screen and (min-width:1024px) {
        .home-page-tests-section-wrapper{
            width: 90% ;
            flex-direction: row;
            justify-content: stretch;
        }
        .home-page-test-rows{
            width: unset ;
            align-self: flex-start;

            &[data-test-row="image"]{
                width: 40% ;
            }

            &[data-test-row="content"]{
                flex: 1;
            }
        }
        .home-page-test-image-container{

            &::before{
                transform: translate(-16%, -60px);
            }
        }
        .home-page-test-image{
            transform: translate(14%, 0px);
        }
    }
</style>