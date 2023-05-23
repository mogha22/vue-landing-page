<template>
    <section class="home-page-call-to-action-section">
        <div class="home-page-call-to-action-wrapper">
            <h3 class="home-page-call-to-action-heading">Get an Appointment</h3>
            <Button type="dark" />
            <p class="home-page-call-to-action-divider">Or</p>
            <p class="home-page-call-to-action-number"><a href="tel:+91-888-999-0000">call us at 0888-999-0000</a></p>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'CallToAction'
    }
</script>

<style lang="scss">
    .home-page-call-to-action-section{
        width: 100% ;
        padding: clamp(85px, 20vh, 150px) 0px ;
        display: flex ;
        flex-direction: column;
        background-image: url('~/assets/images/home/appointment.jpg');
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        background-color: rgba(0, 0, 0, 0.5) ;
        background-blend-mode: darken;
    }
    .home-page-call-to-action-wrapper{
        width: 85% ;
        align-self: center ;
        display: flex ;
        flex-direction: column;
    }
    .home-page-call-to-action-heading{
        font-size: 34px ;
        font-weight: 300 ;
        font-family: var(--font-family);
        text-align: center;
        color: white ;
        padding-bottom: 32px ;
    }
    .home-page-call-to-action-divider{
        font-size: 14px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        text-align: center;
        align-self: center;
        color: white ;
        padding: 32px 0px 24px 0px ;
    }
    .home-page-call-to-action-number{
        font-size: 18px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        text-align: center;
        align-self: center;
        color: white ;

        a{
            text-decoration: none ;
            color: white ;
        }
    }

    @media screen and (min-width: 720px) {
        .home-page-call-to-action-heading{
            font-size: 45px ;
            padding-bottom: 32px ;
        }
        .home-page-call-to-action-divider{
            font-size: 16px ;
            font-weight: 300;
        }
        .home-page-call-to-action-number{
            font-size: 24px ;
        }
    }
</style>