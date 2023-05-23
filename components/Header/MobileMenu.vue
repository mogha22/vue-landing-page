<template>
    <div :data-mobile-menu="menu" class="tvl-mobile-menu-container">
        <div class="tvl-mobile-menu-wrapper">
            <div class="tvl-mobile-menu-header">
                <div v-on:click="mobileMenuDisplay" class="tvl-mobile-menu-header-icon">
                    <span class="material-symbols-outlined">arrow_forward_ios</span>
                </div>
                <div class="tvl-mobile-menu-header-image-container">
                    <p class="tvl-mobile-menu-header-logo">Dr. Jane Doe</p>
                </div>
            </div>
            <div class="tvl-mobile-menu-options-container">
                <div class="tvl-mobile-menu-option">
                    <NuxtLink to="#about">
                        <p class="tvl-mobile-menu-option-text">About</p>
                    </NuxtLink>
                </div>
                <div class="tvl-mobile-menu-option">
                    <NuxtLink to="#packages">
                        <p class="tvl-mobile-menu-option-text">Packages</p>
                    </NuxtLink>
                </div>
                <div class="tvl-mobile-menu-option">
                    <NuxtLink to="#tests">
                        <p class="tvl-mobile-menu-option-text">Tests</p>
                    </NuxtLink>
                </div>
                <div class="tvl-mobile-menu-option">
                    <NuxtLink to="#contact">
                        <p class="tvl-mobile-menu-option-text">Contact</p>
                    </NuxtLink>
                </div>
            </div>
            <div class="tvl-mobile-menu-footer">
                <Button type="dark" />
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'MobileMenu',
        data(){
            return {
                menu:'closed'
            }
        },
        methods: {

            mobileMenuDisplay: function(){

                this.menu = (this.menu === 'closed')? 'open' : 'closed' ;

            }
        }
    }
</script>

<style lang="scss">
    .tvl-mobile-menu-container{
        width: 85% ;
        min-width: 270px ;
        max-width: 320px ;
        height: 100vh;
        position: fixed ;
        top: 0px ;
        right: 0px ;
        display: flex ;
        flex-direction: column;
        padding: 16px 0px ;
        background-color: white;
        z-index: 110;
        transition: 0.25s all ease-in-out;

        &[data-mobile-menu='closed']{
            transform: translateX(100%);
            box-shadow: none;
        }
        &[data-mobile-menu='open']{
            transform: translateX(0%);
            box-shadow: -2px 0px 25px -1px rgba(0, 0, 0, 1);
        }
    }
    .tvl-mobile-menu-wrapper{
        width: 90% ;
        align-self: center;
    }
    .tvl-mobile-menu-header{
        width: 100% ;
        display: flex ;
        flex-direction: row;
        padding: 8px ;
        margin-bottom: 16px ;
        border-radius: 8px ;
        box-sizing: border-box;
    }
    .tvl-mobile-menu-header-icon{
        width: 24px;
        height: 24px ;
        align-self: center;
        box-sizing: border-box;
        color: black;
        cursor: pointer;
        border-radius: 4px ;
        display: flex ;
        flex-direction: column;
        justify-content: center ;

        .material-symbols-outlined{
            font-size: 20px;
        }

        span{
            align-self: center;
        }
    }
    .tvl-mobile-menu-header-image-container{
        flex: 1 ;
        display: flex ;
        flex-direction: column;
        justify-content: center;
    }
    .tvl-mobile-menu-header-logo{
        font-size: 15px ;
        font-weight: 400 ;
        font-family: var(--font-family);
        text-align: center;
        align-self: center;
    }
    .tvl-mobile-menu-options-container{
        width: 100% ;
        display: flex ;
        flex-direction: column;
        //border: 1px solid rgba(0, 0, 0, 0.1);
        border-radius: 8px ;
        margin-bottom: 16px ;
    }
    .tvl-mobile-menu-option{
        width: 95% ;
        padding: 16px 8px ;
        align-self: center;
        display: flex ;
        flex-direction: row;
        border-bottom: 1px solid rgba(0, 0, 0, 0.05);

        a{
            flex: 1;
            text-decoration: none;
            color: black ;
        }
    }
    .tvl-mobile-menu-option-text{
        width: 100% ;
        font-size: 16px ;
        font-weight: 300 ;
        font-family: var(--font-family);
        align-self: center;
    }
    .tvl-mobile-menu-option-icon{
        width: 18px ;
        height: 18px ;
        display: flex ;
        flex-direction: column ;
        align-self: center;
        justify-content: center;
        cursor: pointer;

        span{
            font-size: 18px;
            align-self: center;
        }
    }
    .tvl-mobile-menu-footer{
        width: 100% ;
        display: flex ;
        flex-direction: column;
    }
    .tvl-mobile-menu-sub-options{
        width: 100%;
        padding: 0px 8px ;
        box-sizing: border-box;
        background-color: rgba(245, 245, 245, 0.5);
        overflow: hidden;

        a{
            width: 100% ;
            text-decoration: none;
            color: rgba(0, 0, 0, 0.7) ;
        }
    }
    #tvl-mobile-menu-services-suboption{
        &[data-menu-suboption='closed']{
            height: 0px ;
        }
        &[data-menu-suboption='open']{
            height: auto ;
        }
    }
    #tvl-mobile-menu-industries-suboption{
        &[data-menu-suboption='closed']{
            height: 0px ;
        }
        &[data-menu-suboption='open']{
            height: auto ;
        }
    }
    .tvl-mobile-menu-sub-option-text{
        width: 100% ;
        font-size: 14px ;
        font-weight: 300;
        font-family: var(--font-family);
        padding: 12px 8px;
        box-sizing: border-box;
        border-bottom: 1px solid rgba(0, 0, 0, 0.05);
    }
</style>