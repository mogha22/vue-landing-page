<template>
    <div class="header-desktop-links-container">
        <div :data-link-active="hash" class="header-desktop-links-wrapper">
            <NuxtLink to="#about">
                <p data-link-name="about" class="header-desktop-link">About</p>
            </NuxtLink>
            <NuxtLink to="#packages">
                <p data-link-name="packages" class="header-desktop-link">Packages</p>
            </NuxtLink>
            <NuxtLink to="#tests">
                <p data-link-name="tests" class="header-desktop-link">Tests</p>
            </NuxtLink>
            <NuxtLink to="#contact">
                <p data-link-name="contact" class="header-desktop-link">Contact</p>
            </NuxtLink>
        </div>
    </div>
</template>

<script>
    export default{
        name: 'DesktopLinks',
        data(){
            return {
                hash: ''
            }
        }
    }
</script>

<style lang="scss">
    .header-desktop-links-container{
        width: 100% ;
        align-self: center;
        display: fles ;
        flex-direction: column;
    }
    .header-desktop-links-wrapper{
        width: 300px ;
        display: flex ;
        flex-direction: row;
        justify-content: space-between;

        a.router-link-active{
            text-decoration: none;
            //margin: 0px 8px ;
            align-self: center;
            color: black;
        }

        &[data-link-active='about']{
            .header-desktop-link[data-link-name="about"]{
                text-decoration: underline;
            }
        }

        &[data-link-active='packages']{
            .header-desktop-link[data-link-name="packages"]{
                text-decoration: underline;
            }
        }

        &[data-link-active='tests']{
            .header-desktop-link[data-link-name="tests"]{
                text-decoration: underline;
            }
        }

        &[data-link-active='contact']{
            .header-desktop-link[data-link-name="contact"]{
                text-decoration: underline;
            }
        }
    }
    .header-desktop-link{
        width: fit-content;
        font-size: 14px ;
        font-weight: 500 ;
        font-family: var(--font-family);
        padding: 3px ;

        &:hover{
            text-decoration: underline;
        }
    }
</style>