<template>
    <div class="header-logo-container">
        <NuxtLink to="/">
            <p class="header-logo">Dr. Jane Doe</p>
        </NuxtLink>
    </div>
</template>

<script>
    export default {
        name: 'HeaderLogo'
    }
</script>

<style lang="scss">
    .header-logo-container{
        width: 100% ;
        align-self: flex-start;
    }
    .header-logo{
        font-size: 14px ;
        font-weight: 500;
        text-align: left ;
        color: white ;
        font-family: var(--font-family);
        transition: 0.25s all ease-in-out ;
    }

    @media screen and (min-width:540px) {
        .header-logo{
            font-size: 16px;
        }
    }
</style>
