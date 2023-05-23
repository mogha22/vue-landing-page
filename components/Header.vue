<template>
    <header class="header">
        <div :data-header-state="state" class="header-container">
            <div class="header-wrapper">
                <div data-header-row="header-logo" class="header-wrapper-rows">
                    <HeaderLogo />
                </div>
                <div data-header-row="desktop-links" class="header-wrapper-rows">
                    <HeaderDestopLinks />
                </div>
                <div data-header-row="contact" class="header-wrapper-rows">
                    <HeaderDesktopContact ref="desktopLinks" />
                </div>
                <div data-header-row="mobile-contact" class="header-wrapper-rows">
                    <HeaderMobileContact />
                </div>
                <div data-header-row="menu-icon" class="header-wrapper-rows">
                    <HeaderMobileMenuIcon @mobile-menu-clicked="displayMobileMenu" />
                </div>
            </div>
        </div>
        <HeaderMobileMenu ref="mobileMenu" />
    </header>
</template>

<script>

    export default {
        name: "Header",
        data(){
            return {
                state: 'not-scrolled'
            }
        },
        methods: {
            scrollAnimation(){
                
                this.updateHeaderState((window.pageYOffset > 50)) ;

            },
            updateHeaderState(boolean){

                this.state = (boolean) ? 'scrolled': 'not-scrolled' ;
            },

            displayMobileMenu(){

                this.$refs.mobileMenu.mobileMenuDisplay() ;
            }
        },
        watch: {
            '$route' (to, from){
                
                this.$refs.mobileMenu.menu = 'closed' ;
            }
        }
    }
</script>

<style lang="scss">
    .header{
        width: 100% ;
        height: auto ;
        position: fixed;
        top: 0px ;
        left: 0px ;
        z-index: 100;
    }
    .header-container{
        width: 100% ;
        height: 70px ;
        display: flex ;
        flex-direction: column;
        justify-content: center;
        transition: 0.25s all ease-in-out ;

        &[data-header-state="scrolled"]{
            height: 55px;
            background-color: rgba(255, 255, 255, 0.9);
            box-shadow: 0px 1px 12px -1px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(10px);

            .header-logo{
                color: black ;
            }
        }
    }
    .header-wrapper{
        width: 95% ;
        height: auto ;
        min-width: 290px ;
        align-self: center;
        display: flex ;
        flex-direction: row;
    }
    .header-wrapper-rows{
        align-self: center;
        //display: flex ;
        flex-direction: column;

        &[data-header-row="header-logo"]{
            display: flex;
            flex: 1 ;
        }
        &[data-header-row="desktop-links"]{
            display: none;
        }
        &[data-header-row="contact"]{
            width: 380px ;
            display: none;
        }
        &[data-header-row="mobile-contact"]{
            width: 100px ;
            display: flex;
        }
        &[data-header-row="menu-icon"]{
            display: flex;
            width: 35px ;
        }
    }

    @media screen and (min-width:720px) {
        .header-wrapper-rows{

            &[data-header-row="contact"]{
                display: flex;
            }
            &[data-header-row="mobile-contact"]{
                display: none;
            }
        }
    }

    @media screen and (min-width:1200px) {

        .header-wrapper-rows{

            &[data-header-row="desktop-links"]{
                display: flex;
                width: 33%;
            }
            &[data-header-row="contact"]{
                width: 33%;
            }
            &[data-header-row="menu-icon"]{
                display: none;
            }
        }
    }
</style>