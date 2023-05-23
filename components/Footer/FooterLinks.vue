<template>
    <div class="footer-links-container">
        <div class="footer-links-wrapper">
            <div class="footer-links-columns">
                <h3 class="footer-links-heading">Company</h3>
                <div class="footer-links-options">
                    <NuxtLink to="#about">
                        <p class="footer-links-option">About</p>
                    </NuxtLink>
                    <NuxtLink to="#packages">
                        <p class="footer-links-option">Packages</p>
                    </NuxtLink>
                    <NuxtLink to="#tests">
                        <p class="footer-links-option">Tests</p>
                    </NuxtLink>
                </div>
            </div>
            <div class="footer-links-columns">
                <h3 class="footer-links-heading">Services</h3>
                <div class="footer-links-options">
                    <p class="footer-links-option">Class II Medical</p>
                    <p class="footer-links-option">Consultation</p>
                    <p class="footer-links-option">Lab Tests</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'FooterLinks',
    }
</script>

<style lang="scss">
    .footer-links-container{
        width: 100% ;
        margin: 75px 0px 45px 0px;
        align-self: center;
        display: flex;
        flex-direction: column;
    }
    .footer-links-wrapper{
        width: 100% ;
        max-width: 300px;
        align-self: center;
        display: flex ;
        flex-direction: column;
    }
    .footer-links-columns{
        width: 130px ;
        align-self: center;
        display: flex ;
        flex-direction: column;
        margin-bottom: 32px ;
    }
    .footer-links-heading{
        font-size: 18px ;
        font-weight: 500 ;
        font-family: var(--font-family);
        text-align: center;
        color: white ;
    }
    .footer-links-options{
        width: 100% ;
        align-self: center;
        margin: 24px 0px 16px 0px ;
    }
    .footer-links-option{
        font-size: 16px ;
        font-family: var(--font-family);
        font-weight: 300;
        color: white ;
        text-align: center;
        padding: 4px 0px ;
        margin-bottom: 4px ;
    }

    @media screen and (min-width: 540px) {
        .footer-links-wrapper{
            flex-direction: row;
            justify-content: space-around;
        }
    }

    @media screen and (min-width:720px) {
        .footer-links-wrapper{
            align-self: flex-start;
        }
        .footer-links-heading{
            text-align: left;
        }
        .footer-links-option{
            text-align: left;
        }
    }

    @media screen and (min-width: 1200px) {
        .footer-links-wrapper{
            align-self: center;
        }
    }
</style>