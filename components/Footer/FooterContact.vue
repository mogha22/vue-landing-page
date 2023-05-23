<template>
    <div id="contact" class="footer-contact-container">
        <div class="footer-contact-wrapper">
            <h1 class="footer-contact-heading">Contact</h1>
            <div class="footer-contact-options">
                <p class="footer-contact-option">
                    <span class="material-symbols-outlined">mail</span>
                    <span>&nbsp;&nbsp;hello@drjane.com</span>
                </p>
                <p class="footer-contact-option">
                    <span class="material-symbols-outlined">call</span>
                    <span><a href="tel:+91-888-999-0000">&nbsp;&nbsp;+91 888-999-0000</a></span>
                </p>
                <p class="footer-contact-option">
                    <span class="material-symbols-outlined">location_on</span>
                    <span>&nbsp;&nbsp;19, Dwarka, New Delhi</span>
                </p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'FooterContact'
    }
</script>

<style lang="scss">
    .footer-contact-container{
        width: 100% ;
        margin: 75px 0px 45px 0px;
        align-self: center;
        display: flex ;
        flex-direction: column;
    }
    .footer-contact-wrapper{
        width: 220px ;
        align-self: center;
        display: flex ;
        flex-direction: column;
    }
    .footer-contact-heading{
        font-size: 20px ;
        font-weight: 500 ;
        font-family: var(--font-family);
        text-align: center;
        color: white ;
    }
    .footer-contact-options{
        width: 100% ;
        align-self: center;
        margin: 24px 0px 16px 0px ;
    }
    .footer-contact-option{
        font-size: 16px ;
        font-family: var(--font-family);
        font-weight: 300;
        color: white ;
        text-align: center;
        padding: 5px 0px ;
        margin-bottom: 7px ;
        line-height: 1;

        .material-symbols-outlined{
            font-size: 18px ;
            font-variation-settings:'FILL' 0 ;
            transform: translateY(-1px);
        }

        span{
            display: inline-block;
            vertical-align: middle;

            a{
                color: white ;
                text-decoration: none;
            }
        }
    }

    @media screen and (min-width: 720px) {
        .footer-contact-wrapper{
            align-self: flex-end;
        }
        .footer-contact-heading{
            text-align: left;
        }
        .footer-contact-option{
            text-align: left;
        }
    }
</style>