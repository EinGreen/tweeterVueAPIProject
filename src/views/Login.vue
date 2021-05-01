<template>
    <div>
        <login-options></login-options>
        <signup-menu></signup-menu>
        <login-menu></login-menu>
    </div>
</template>

<script>
    import LoginOptions from "../components/LoginOptions.vue";
    import SignupMenu from "../components/SignupMenu.vue";
    import LoginMenu from "../components/LoginMenu.vue";

    export default {
        name: 'login',
        components: {
            LoginMenu,
            SignupMenu,
            LoginOptions,
        },
    }
</script>

<style scoped>
    
</style>