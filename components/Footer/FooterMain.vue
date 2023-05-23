<template>
    <div class="footer-main">
        <div class="footer-main-wrapper">
            <div data-main-column="logo" class="footer-main-columns">
                <FooterLogo />
            </div>
            <div data-main-column="nav" class="footer-main-columns">
                <div class="footer-main-columns-wrapper">
                    <div data-column-row="link" class="footer-main-column-rows">
                        <FooterLinks />
                    </div>
                    <div data-column-row="contact" class="footer-main-column-rows">
                        <FooterContact />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'FotoerMain'
    }
</script>

<style lang="scss">
    .footer-main{
        width: 100% ;
        display: flex ;
        flex-direction: column;
        padding: clamp(20px, 8vh, 50px) 0px ;
    }
    .footer-main-wrapper{
        width: 90% ;
        align-self: center;
        display: flex ;
        flex-direction: column;
    }
    .footer-main-columns{
        width: 90% ;
        align-self: center;
        display: flex ;
        flex-direction: column;
    }
    .footer-main-columns-wrapper{
        width: 100% ;
        display: flex ;
        flex-direction: column;
    }
    .footer-main-column-rows{
        width: 100% ;
        align-self: center;
    }

    @media screen and (min-width: 720px) {
        .footer-main-columns-wrapper{
            flex-direction: row;
        }
        .footer-main-column-rows{
            width: 50% ;
            align-self: flex-start;
        }
    }

    @media screen and (min-width:1200px) {
        .footer-main-wrapper{
            width: 90% ;
            flex-direction: row;
        }
        .footer-main-columns{
            width: unset;
            align-self: flex-start;

            &[data-main-column="logo"]{
                width: 35% ;
            }

            &[data-main-column="nav"]{
                flex: 1 ;
            }
        }
    }
</style>