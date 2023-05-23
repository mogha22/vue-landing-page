<template>
    <footer class="footer">
        <div class="footer-wrapper">
            <FooterMain />
            <div class="footer-devs-section">
                <div class="footer-devs-wrapper">
                    <a href="https://www.thevervelabs.com" target="_blank" class="footer-devs-anchor">
                        <p class="footer-devs-name">Design & Developed by <img src="~/assets/images/footer/logo.png" alt="the verve labs" class="footer-devs-logo"> <strong>The Verve Labs</strong></p>
                    </a>
                </div>
            </div>
            <FooterBottom />
        </div>
    </footer>
</template>

<script>
    export default {
        name: 'Footer'
    }
</script>

<style lang="scss">
    .footer, .footer-wrapper{
        width: 100% ;
        display: flex ;
        flex-direction: column;
        background-color: #081925;
    }
    .footer-devs-section{
        width: 90% ;
        min-width: 280px ;
        align-self: center;
        display: flex ;
        flex-direction: column;
        margin-bottom: 16px ;
    }
    .footer-devs-wrapper{
        width: fit-content ;
        align-self: center;
        padding: 4px 0px ;
        box-sizing: border-box;
    }
    .footer-devs-anchor{
        width: fit-content;
        text-decoration: none;
    }
    .footer-devs-name{
        width: fit-content ;
        font-size: 13px ;
        font-weight: 300 ;
        font-family: var(--font-family);
        text-align: center;
        color: white ;
        position: relative;

        img{
            display: inline-block;
            vertical-align: middle;
            width: 25px ;
            height: auto ;
            margin: 0px 5px ;
            transform: translateY(-1px);
        }
    }

    @media screen and (min-width: 720px) {
        .footer-devs-wrapper{
            align-self: flex-start;
        }
    }
</style>

