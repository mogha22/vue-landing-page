<template>
    <section id="packages" class="home-page-packages-section">
        <div class="home-page-packages-wrapper">
            <h2 class="home-page-packages-heading">Packages</h2>
            <div class="home-page-packages-container">
                <div v-for="(list, key) in lists" :key="key" class="home-page-packages-card-container">
                    <div :data-popular="list.suited" class="home-page-package-popular">
                        <p class="home-page-package-popular-text">
                            <span class="material-symbols-outlined">star</span>
                            <span>Most Popular</span>
                        </p>
                    </div>
                    <IndexPackagesCard 
                        :name="list.name"
                        :description="list.description"
                        :tests="list.tests"
                    />
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'Packages',
        data(){
            return {
                lists: [
                            {
                                name: 'consult',
                                description: 'Best suited for',
                                color: '#FF8383',
                                suited: false,
                                tests: [
                                            'General Examination',
                                            'Lab Investigations',
                                            'Any other test deemed fit based on history/clinial examination'
                                        ]
                            },
                            {
                                name: 'pro',
                                description: 'Pro package contains end to end solution ( one stop solution )',
                                color: '#8583FF',
                                suited: true,
                                tests: [
                                            'General Examination',
                                            'Lab Investigations',
                                            'Eye Examination',
                                            'ENT Examination',
                                            'Any other test deemed fit based on history/clinial examination'
                                        ]
                            }
                        ]
            }
        }
    }
</script>

<style lang="scss">
    .home-page-packages-section{
        width: 100% ;
        display: flex ;
        flex-direction: column;
        padding: clamp(50px, 15vh, 90px) 0px ;
    }
    .home-page-packages-wrapper{
        width: 90% ;
        align-self: center;
        display: flex ;
        flex-direction: column;
    }
    .home-page-packages-heading{
        font-size: 35px ;
        font-weight: 400 ;
        font-family: var(--font-family) ;
        text-align: center;
        align-self: center ;
    }
    .home-page-packages-container{
        width: 90% ;
        display: flex ;
        flex-direction: column;
        align-self: center;
        padding-top: 48px ;
    }
    .home-page-package-popular{
        width: 65% ;
        min-width: 270px ;
        align-self: center;
        margin: 0px 0px 6px 0px ;
        display: flex ;
        flex-direction: column;
        cursor: default;
        opacity: 0;

        &[data-popular=true]{
            opacity: 1;
        }
    }
    .home-page-package-popular-text{
        width: fit-content;
        font-size: 12px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        color: white ;
        padding: 4px 10px ;
        background-color: black;
        border-radius: 25px ;
        align-self: flex-start;
        //margin-left: 12px ;

        .material-symbols-outlined{
            font-size: 14px;
            color: #FFD600 ;
            transform: translateY(-1px);
        }

        span{
            display: inline-block ;
            vertical-align: middle;
        }
    }
    .home-page-packages-card-container{
        width: 100% ;
        display: flex;
        flex-direction: column;
        margin: 16px 0px ;
        align-self: center;
    }

    @media screen and (min-width:720px) {
        .home-page-packages-container{
            flex-direction: row;
            max-width: 950px ;
            justify-content: stretch;
        }
        .home-page-packages-card-container{
            width: 50% ;
            align-self: unset;
        }
    }
</style>