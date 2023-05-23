<template>
    <div v-on:click="$emit('mobile-menu-clicked')" class="menu-icon-container">
        <img src="~/assets/images/header/menu.png" alt="menu-icon" class="menu-icon">
    </div>
</template>

<script>
    export default {
        name: 'MobileMenuIcon'
    }
</script>

<style lang="scss">
    .menu-icon-container{
        width: 100% ;
        display: flex ;
        flex-direction: column;
    }
    .menu-icon{
        width: 30px ;
        height: auto ;
        align-self: flex-end;
        //filter: invert(100%) ;
        cursor: pointer;
    }
</style>