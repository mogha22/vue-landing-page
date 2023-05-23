<template>
    <div class="hero-content-about">
        <div class="hero-content-about-wrapper">
            <div class="hero-content-about-image-container">
                <img src="~/assets/images/home/hero/doc-image-1.jpg" alt="" class="hero-content-about-image">
            </div>
        </div>
        <p class="hero-content-about-tag">Dr. Jane Doe - MBBS, PGDEMS</p>
        <div class="hero-content-about-certs-container">
            <div v-for="cert in certs" class="hero-content-about-cert">
                <p class="hero-content-about-cert-icon"><span class="material-symbols-outlined">verified_user</span></p>
                <p class="hero-content-about-cert-name">{{ cert.name }}</p>
                <p class="hero-content-about-cert-by">{{ cert.by }}</p>
                <p v-if="cert.tag !== ''" class="hero-content-about-cert-tag">( {{ cert.tag }} )</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'HeroContentAbout',
        data(){
            return {

                certs: [
                            {
                                name: 'MRO Certified',
                                by: 'by AOCOPM USA',
                                tag: ''
                            },
                            {
                                name: 'Aero Medical Examiner',
                                by: 'by DGCA',
                                tag: 'Class II'
                            },

                        ]
            }
        }
    }
</script>

<style lang="scss">
    .hero-content-about{
        width: 100% ;
        display: flex ;
        flex-direction: column;
    }
    .hero-content-about-wrapper{
        width: 90% ;
        align-self: center;
        display: flex ;
        flex-direction: column;
    }
    .hero-content-about-image-container{
        width: 250px ;
        height: auto ;
        margin: 32px 0px ;
        align-self: center;
        position: relative;
        z-index: 1;

        &::before{
            content: '' ;
            width: 250px ;
            height: 250px ;
            border-radius: 100% ;
            background-color: #9E00FF;
            filter: blur(5px) ;
            position: absolute;
            top: 0px ;
            left: 0px ;
            transform: translate(5%, -2.5%);
            z-index: -1;
            animation: bottomBlur 1.6s ease-in-out infinite ;
        }
        &::after{
            content: '' ;
            width: 250px ;
            height: 250px ;
            border-radius: 100% ;
            background-color: #FD8DFF;
            filter: blur(5px) ;
            position: absolute;
            top: 0px ;
            left: 0px ;
            transform: translate(-5%, 2.5%);
            z-index: -1;
            animation: topBlur 1.6s ease-in-out infinite ;
        }
    }

    @keyframes topBlur {
        0%{
            background-color: #FD8DFF;
        }
        50%{
            background-color: #9E00FF;
        }
        100%{
            background-color: #FD8DFF;
        }
        // 0% {
        //     transform: translate(5%, -2.5%);
        // }
        // 50%{
        //     transform: translate(-5%, 2.5%);
        // }
        // 100%{
        //     transform: translate(5%, -2.5%);
        // }
    }

    @keyframes bottomBlur {
        0%{
            //background-color: #FD8DFF;
            background-color: #9E00FF;
        }
        50%{
            background-color: #FD8DFF;
        }
        100%{
            //background-color: #FD8DFF;
            background-color: #9E00FF;
        }
        // 0%{
        //     transform: translate(-5%, 2.5%);
        // }
        // 50%{
        //     transform: translate(5%, -2.5%);
        // }
        // 100%{
        //     transform: translate(-5%, 2.5%);
        // }
    }
    .hero-content-about-image{
        width: 100% ;
        height: auto ;
        border-radius: 100% ;
    }
    .hero-content-about-tag{
        width: fit-content ;
        align-self: center;
        font-size: 13px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        padding: 4px 16px 3px 16px;
        color: #FFFFFF ;
        border-radius: 40px ;
        box-sizing: border-box;
        background-color: #15405D;
    }
    .hero-content-about-certs-container{
        width: 280px ;
        display: flex ;
        flex-direction: row;
        justify-content: space-between;
        margin: 32px 0px 32px 0px ;
        align-self: center;
    }
    .hero-content-about-certs{
        width: 45% ;
        align-self: flex-start;
        display: flex ;
        flex-direction: column;
    }
    .hero-content-about-cert-icon{
        align-self: center;
        text-align: center;

        .material-symbols-outlined{
            font-size: 24px ;
            color: #56AB00 ;
        }
    }
    .hero-content-about-cert-name{
        font-size: 14px ;
        font-weight: 500 ;
        font-family: var(--font-family);
        text-align: center;
        align-self: center;
        color: black ;
        margin-bottom: 4px ;
    }
    .hero-content-about-cert-by{
        font-size: 12px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        text-align: center;
        align-self: center;
        color: #626262 ;
        margin-bottom: 8px ;
    }
    .hero-content-about-cert-tag{
        font-size: 13px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        text-align: center;
        align-self: center;
    }

    @media screen and (min-width:1100px) {
        .hero-content-about-image-container{
            width: 300px ;

            &::before{
                content: '' ;
                width: 300px ;
                height: 300px ;
                //transform: translate(15px, -10px);
            }
            &::after{
                content: '' ;
                width: 300px ;
                height: 300px ;
                //transform: translate(-15px, 10px);
            }
        }
        .hero-content-about-tag{
            font-size: 14px ;
        }
        .hero-content-about-certs-container{
            width: 300px ;
        }
    }
</style>