<template>
    <div>
        <option-menu></option-menu>
        <sign-up></sign-up>
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