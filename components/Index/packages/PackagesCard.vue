<template>
    <div :data-card-type="name" class="home-page-package-card">
        <div class="home-page-package-card-header">
            <p class="home-page-package-card-name">{{ name }}</p>
        </div>
        <div class="home-page-package-card-body">
            <p class="home-page-package-card-desc">{{ description }}</p>
            <div class="home-page-package-button">
                <a href="" class="home-page-package-button-anchor">
                    <p class="home-page-package-button-text">Book an Appointment</p>
                </a>
            </div>
            <div class="home-page-package-card-tests">
                <p v-for="test in tests" class="home-page-package-card-test">
                    <span class="material-symbols-outlined">check_circle</span>
                    {{ test }}
                </p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'PackagesCard',
        props: {
            name: String,
            description: String,
            tests: Array,
            color: String
        }
    }
</script>

<style lang="scss">
    .home-page-package-card{
        width: 65% ;
        min-width: 270px ;
        height: 100% ;
        border-radius: 20px ;
        overflow: hidden;
        align-self: center;
        margin-bottom: 40px ;
        display: flex ;
        flex-direction: column;

        &[data-card-type="consult"]{
            border: 1px solid #FF8383 ;

            .home-page-package-card-name{
                color: #FF8383  ;
            }
            .home-page-package-card-body{
                background-color: #FF8383 ;
            }
            .home-page-package-button-text{
                color: #FF8383 ;
            }
        }

        &[data-card-type="pro"]{
            border: 1px solid #8583FF ;

            .home-page-package-card-name{
                color: #8583FF ;
            }
            .home-page-package-card-body{
                background-color: #8583FF;
            }
            .home-page-package-button-text{
                color: #8583FF ;
            }
        }
    }
    .home-page-package-card-header{
        width: 100% ;
        padding: 16px 16px ;
        box-sizing: border-box;
    }
    .home-page-package-card-name{
        font-size: 22px ;
        font-weight: 500 ;
        text-align: left;
        font-family: var(--font-family);
        text-transform: capitalize;
        padding: 0px 8px ;
        box-sizing: border-box;
    }
    .home-page-package-card-body{
        width: 100% ;
        flex: 2;
        padding: 24px 16px ;
        box-sizing: border-box;
    }
    .home-page-package-card-desc{
        font-size: 15px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        text-align: left;
        box-sizing: border-box;
        color: white ;
    }
    .home-page-package-button{
        width: fit-content;
        background-color: white;
        overflow: hidden;
        border-radius: 25px ;
        margin-top: 16px ;
    }
    .home-page-package-button-anchor{
        text-decoration: none;
    }
    .home-page-package-button-text{
        font-size: 13px ;
        font-weight: 500 ;
        font-family: var(--font-family);
        padding: 4px 18px ;
    }
    .home-page-package-card-tests{
        width: 100% ;
        padding: 24px 0px 12px 0px;
        box-sizing: border-box;
    }
    .home-page-package-card-test{
        font-size: 15px ;
        font-weight: 400;
        font-family: var(--font-family);
        color: white;
        padding: 3px 0px ;
        margin-bottom: 8px ;
        display: flex ;
        flex-direction: row;
        line-height: 1.5;

        .material-symbols-outlined{
            font-size: 19px ;
            color: white ;
            transform: translateY(1px);
            padding-right: 5px ;
        }

        span{
            display: inline-block;
            vertical-align: middle;
        }
    }
</style>