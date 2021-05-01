<template>
    <div>
        <form action="javascript:void(0)" id="signMenu">
            <h3>Sign Up: </h3>
            <!-- user input -->
            <input type="text" id="usernameInput" placeholder="username">
            <input type="text" id="emailInput" placeholder="email">
            <input type="text" id="passwordInput" placeholder="password">
            <!-- Submit button -->
            <input type="submit" value="Submit">
        </form>
        <p>{{ signupStatus }}</p>
    </div>
</template>

<script>
    import axios from "axios";
    // import cookies from "vue-cookies";

    export default {
        name: "signup-menu",
        data() {
            return {
                signupStatus: '',
                // signupStatus will show a message of the the account creation process
            }
        },
        methods: {
            // this function crates an account:
            createAccount() {
                this.signupStatus = "Creating Account...";
                axios.request({
                    url: "https://tweeterest.ml/api/users",
                    method: "POST",
                    headers: {
                        "Content-Type": "application/json",
                        "X-Api-Key": `${process.env.VUE.VUE_APP_API_KEY}`
                    },
                    data: {
                        username: document.getElementById("usernameInput").value,
                        email: document.getElementById("emailInput").value,
                        password: document.getElementById("passwordInput").value,
                    },
                }).then((res) => {
                    this.signupStatus = "Account Created";
                    console.log(res);
                }).catch((err) => {
                    this.signupStatus = "failed to create account";
                    console.log(err);
                });
            }
        },
    }
</script>

<style scoped>

</style>