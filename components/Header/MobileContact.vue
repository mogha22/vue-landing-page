<template>
    <div class="header-mobile-contact-container">
        <div class="header-mobile-contact-wrapper">
            <a href="tel:+91-888-999-0000" data-button="book" class="header-mobile-contact-button">
                <p class="header-mobile-contact-button-icon">
                    <span class="material-symbols-outlined">call</span>
                </p>
            </a>
            <div data-button="book" class="header-mobile-contact-button">
                <a href="">
                    <p class="header-mobile-contact-button-icon">
                        <span class="material-symbols-outlined">calendar_month</span>
                    </p>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'MobileContact'
    }
</script>

<style lang="scss">
    .header-mobile-contact-container{
        width: 100% ;
        align-self: center;
        display: flex ;
        flex-direction: column;
    }
    .header-mobile-contact-wrapper{
        width: 100% ;
        display: flex ;
        flex-direction: row;
        justify-content: space-around;
    }
    .header-mobile-contact-button{
        width: 35px ;
        height: 35px ;
        display: flex ;
        flex-direction: row ;
        justify-items: center;
        border-radius: 100% ;
        overflow: hidden;
        box-sizing: border-box;

        &[data-button="call"]{
            border: 1px solid #1D5982 ;
            background-color: white;

            .header-mobile-contact-button-icon{
                .material-symbols-outlined{
                    color: #1D5982 ;
                }
            }
        }

        &[data-button="book"]{
            background-color: #1D5982 ;

            .header-mobile-contact-button-icon{
                .material-symbols-outlined{
                    color: white;
                }
            }
        }

        a{
            align-self: center;
            margin: 0px auto ;
        }
    }
    .header-mobile-contact-button-icon{
        width: 100% ;
        text-align: center;
        align-self: center;

        .material-symbols-outlined{
            font-size: 18px ;
        }

        span{
            display: inline-block;
            vertical-align: middle;
            transform: translateY(-1px);
        }
    }
</style>