<template>
    <div>
        <form action="javascript:void(0)" id="logMenu">
            <h3>Login: </h3>
            <input type="text">
        </form>
    </div>
</template>

<script>
    export default {
        name: 'login-menu',
    }
</script>

<style scoped>
    #logMenu {
        display: grid;
        justify-content: center;
    }

    form {
        border: 1px solid;
    } 
</style>