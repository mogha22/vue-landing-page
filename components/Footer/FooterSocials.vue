<template>
    <div class="footer-socials-container">
        <div class="footer-socials-icon">
            <a href="/" class="footer-socials-anchor">
                <img src="~/assets/images/footer/socials/facebook.png" alt="facebook" class="footer-socials-icon-image">
            </a>
        </div>
        <div class="footer-socials-icon">
            <a href="/" class="footer-socials-anchor">
                <img src="~/assets/images/footer/socials/instagram.png" alt="instagram" class="footer-socials-icon-image">
            </a>
        </div>
        <div class="footer-socials-icon">
            <a href="/" class="footer-socials-anchor">
                <img src="~/assets/images/footer/socials/twitter.png" alt="twitter" class="footer-socials-icon-image">
            </a>
        </div>
        <div class="footer-socials-icon">
            <a href="/" class="footer-socials-anchor">
                <img src="~/assets/images/footer/socials/linkedin.png" alt="linkedin" class="footer-socials-icon-image">
            </a>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'FooterSocials'
    }
</script>

<style lang="scss">
    .footer-socials-container{
        width: 220px ;
        align-self: center;
        display: flex ;
        flex-direction: row;
        justify-content: space-between;
        margin-top: 40px ;
    }
    .footer-socials-icon{
        width: 22px ;
        height: auto ;
        align-self: center;
    }
    .footer-socials-anchor{
        text-decoration: none;
    }
    .footer-socials-icon-image{
        width: 100% ;
        height: auto ;
    }
</style>