<template>
    <section id="about" class="home-page-about-section">
        <div class="home-page-about-section-wrapper">
            <img src="~/assets/images/home/hero/doc-image-2.png" alt="" class="home-page-about-section-image">
            <h2 class="home-page-about-section-heading">About <br>Dr. Jane Doe</h2>
            <p class="home-page-about-section-text">Dr. Jane is a highly educated and experienced female doctor who is renowned for her exceptional medical expertise. She is a certified medical examiner by the Directorate General of Civil Aviation, providing Class 2 medical certifications to cabin crews in a seamless and hassle-free manner, providing reports within 24-48 hours.</p>
            <div class="home-page-about-certs-container">
                <div data-cert-row="school" class="home-page-about-certs-rows">
                    <div v-for="school in schools" class="home-page-about-cert">
                        <p class="home-page-about-cert-icon"><span class="material-symbols-outlined">school</span></p>
                        <p class="home-page-about-cert-name">{{ school }}</p>
                    </div>
                </div>
                <div data-cert-row="badge" class="home-page-about-certs-rows">
                    <div v-for="cert in certs" class="home-page-about-cert">
                        <p class="home-page-about-cert-icon"><span class="material-symbols-outlined">verified_user</span></p>
                        <p class="home-page-about-cert-name">{{ cert.name }}</p>
                        <p class="home-page-about-cert-by">{{ cert.by }}</p>
                        <p v-if="cert.tag !== ''" class="home-page-about-cert-tag">( {{ cert.tag }} )</p>
                    </div>
                </div>
            </div>
            <Button type="dark" />
            <MetricsSection />
        </div>
    </section>
</template>

<script>
    import MetricsSection from '../metrics/MetricsSection.vue';
    export default {
        name: 'AboutSection',
        components:{MetricsSection},
        data(){
            return {
                schools: [ 'MBBS', 'PGDEMS' ],
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
                            }
                        ]
            }
        }
    }
</script>

<style lang="scss">
    .home-page-about-section{
        width: 100% ;
        display: flex ;
        flex-direction: column;
        padding: clamp(35px, 10vh, 80px) 0px ;
        background-color: white ;
    }
    .home-page-about-section-wrapper{
        width: 90% ;
        //max-width: 400px ;
        display: flex ;
        flex-direction: column;
        align-self: center;
        padding: clamp(15px, 8vh, 30px) 0px ;
    }
    .home-page-about-section-image{
        width: 60px ;
        height: auto ;
        align-self: center;
        margin-bottom: 8px ;
    }
    .home-page-about-section-heading{
        font-size: 32px ;
        font-weight: 300 ;
        font-family: var(--font-family);
        text-align: center;
        line-height: 1.5;
    }
    .home-page-about-section-text{
        width: 90% ;
        max-width: 500px ;
        font-size: 14px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        text-align: center;
        line-height: 1.45;
        align-self: center;
        padding: 32px 0px ;
    }
    .home-page-about-certs-container{
        width: 280px ;
        display: flex ;
        flex-direction: column;
        margin: 16px 0px 32px 0px ;
        align-self: center;
    }
    .home-page-about-certs-rows{
        width: 100% ;
        display: flex ;
        flex-direction: row;
        justify-content: space-between;
        margin: 12px 0px 12px 0px ;
    }
    .home-page-about-cert{
        width: 47% ;
        display: flex ;
        flex-direction: column;
        align-self: flex-start;
    }
    .home-page-about-cert-icon{
        color: #56AB00 ;
        text-align: center;
        align-self: center;
        margin-bottom: 8px ;

        .material-symbols-outlined{
            font-size: 24px ;
        }
    }
    .home-page-about-cert-name{
        font-size: 14px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        text-align: center;
        align-self: center;
        margin-bottom: 4px ;
    }
    .home-page-about-cert-by{
        font-size: 12px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        text-align: center;
        align-self: center;
        color: #626262 ;
        margin-bottom: 6px ;
    }
    .home-page-about-cert-tag{
        font-size: 13px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        color: black ;
        text-align: center;
        align-self: center;
    }

    @media screen and (min-width:540px ) {
        .home-page-about-certs-container{
            width: 520px ;
            flex-direction: row;
            justify-content: space-between;
        }
        .home-page-about-certs-rows{
            width: unset;
            align-self: flex-start;

            &[data-cert-row="school"]{
                width: 230px ;
            }

            &[data-cert-row="badge"]{
                flex: 1;
            }
        }
    }

    @media screen and (min-width: 720px) {
        .home-page-about-certs-container{
            width: 550px ;
        }
        
    }
</style>