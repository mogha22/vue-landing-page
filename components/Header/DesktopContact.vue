<template>
    <div class="header-desktop-contact-container">
        <div class="header-desktop-contact-wrapper">
            <a href="tel:+91-888-999-0000" class="header-desktop-contact-anchor">
                <p class="header-desktop-contact-call">
                    <span class="material-symbols-outlined">call</span>
                    <span>+91-888-999-0000</span>
                </p>
            </a>
            <Button type="dark" placement="header" />
        </div>
    </div>
</template>

<script>
    export default {
        name: 'DesktopConact'
    }
</script>

<style lang="scss">
    .header-desktop-contact-container{
        width: 100% ;
        max-width: 400px ;
        align-self: flex-end;
        display: flex ;
        flex-direction: column;
    }
    .header-desktop-contact-wrapper{
        width: 100% ;
        display: flex ;
        flex-direction: row;
        justify-content: space-around;

        a{
            align-self: center;
            color: #1D5982;
        }
    }
    .header-desktop-contact-call{
        width: fit-content;
        font-size: 15px ;
        font-weight: 500 ;
        font-family: var(--font-family);
        color: #1D5982;
        padding: 4px ;
        box-sizing: border-box;
        align-self: center;

        .material-symbols-outlined{
            font-size: 18px ;
            color: #1D5982 ;
            transform: translateY(-1px);
            padding-right: 7px ;
        }

        span{
            display: inline-block ;
            vertical-align: middle;
        }
    }

    @media screen and (min-width:1200px) {
        .header-desktop-contact-container{
            max-width: 380px ;
        }
        .header-desktop-contact-wrapper{
            justify-content: space-between;
        }
    }
</style>