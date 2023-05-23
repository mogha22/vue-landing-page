<template>
    <div class="footer-bottom">
        <div class="footer-bottom-wrapper">
            <div class="footer-bottom-rows">
                <div class="footer-bottom-text-container">
                    <p class="footer-bottom-text">Dr. Jane Doe &#169;&nbsp;</p>
                    <p class="footer-bottom-text">Copyright . 2023 . All rights reserved</p>
                </div>
            </div>
            <div class="footer-bottom-rows">
                <div class="footer-bottom-link-container">
                    <NuxtLink to="/"><p class="footer-bottom-text">Cookie Policy</p></NuxtLink>
                    <NuxtLink to="/"><p class="footer-bottom-text">Privacy Policy</p></NuxtLink>
                    <NuxtLink to="/"><p class="footer-bottom-text">Terms of Use</p></NuxtLink>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'FooterBottom'
    }
</script>

<style lang="scss">
    .footer-bottom{
        width: 100% ;
        padding: 8px;
        box-sizing: border-box;
        background-color: #15405D;
    }
    .footer-bottom-wrapper{
        width: 100% ;
        display: flex ;
        flex-direction: column;
    }
    .footer-bottom-rows{
        width: 100% ;
        display: flex ;
        flex-direction: column;
    }
    .footer-bottom-text-container{
        width: 100% ;
        align-self: center;
        margin: 16px 0px ;
    }
    .footer-bottom-link-container{
        align-self: center;

        a.router-link-active{
            padding: 0px 3px ;
            margin: 0px 3px ;
        }
    }
    .footer-bottom-text{
        font-size: 12px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        color: white ;
        text-align: center;
        padding: 2px 0px ;
        margin: 4px 0px ;

    }

    @media screen and (min-width: 720px) {
        .footer-bottom-wrapper{
            flex-direction: row;
        }
        .footer-bottom-rows{
            width: 50% ;
        }
        .footer-bottom-text-container{
            margin: 0px ;
        }
        .footer-bottom-link-container{
            align-self: flex-end;
        }
        .footer-bottom-text{
            display: inline-block;
            vertical-align: middle;
            padding: 0px ;
            margin: 0px ;
        }
    }
</style>