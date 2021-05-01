<template>
    <div>
        <form action="javascript:void(0)" id="logMenu">
            <h3>Login: </h3>
            <!-- user input -->
            <input type="text" id="usernameInput" placeholder="username">
            <input type="text" id="emailInput" placeholder="email">
            <input type="text" id="passwordInput" placeholder="password">
            <!-- Submit button -->
            <input type="submit" value="Submit">
        </form>
    </div>
</template>

<script>
    import axios from "axios";
    // import cookies from "vue-cookies";

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
                    url: "https://tweeterest.ml/api/users",
                    method: "GET",
                    headers: {
                        "X-Api-Key": `${process.env.VUE.VUE_APP_API_KEY}`
                    }
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