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
        data() {
            return {
                loginStatus: '',
            }
        },
        methods: {
            atteptLogin() {
                this.loginStatus = "Loading..."
                axios.request({
                    // Insert Url, and Method Here
                }).then((res) => {
                    console.log(res);
                }).catch((err) => {
                    console.log(err);
                });
            }
        },
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