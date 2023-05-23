<template>
    <div class="footer-logo-container">
        <h2 class="footer-logo-subheading">Dr. Jane Doe’s</h2>
        <p class="footer-logo-heading">Clinic</p>
        <FooterSocials />
    </div>
</template>

<script>
    export default {
        name: 'FooterLogo'
    }
</script>

<style lang="scss">
    .footer-logo-container{
        width: 230px ;
        align-self: center;
        display: flex ;
        flex-direction: column;
        margin: 75px 0px 45px 0px;
    }
    .footer-logo-subheading{
        font-size: 17px ;
        font-weight: 300 ;
        font-family: var(--font-family);
        text-align: center;
        color: white ;
        text-transform: uppercase;
    }
    .footer-logo-heading{
        font-size: 60px;
        font-weight: 400 ;
        font-family: 'Baskervville', sans-serif;
        text-align: center;
        color: white ;
        text-transform: uppercase;
        line-height: 1.2;
    }

    @media screen and (min-width:1024px) {
        .footer-logo-container{
            align-self: flex-start;
        }
    }
</style>
