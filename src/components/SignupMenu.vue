<template>
    <div>
        <form action="javascript:void(0)" id="signMenu">
            <h3>Sign Up: </h3>
            <!-- user input -->
            <input type="text" placeholder="username">
            <input type="text" placeholder="email">
            <input type="text" placeholder="password">
            <!-- Submit button -->
            <input type="submit" value="Submit">
        </form>
        <p>{{ signupStatus }}</p>
    </div>
</template>

<script>
    export default {
        name: "sign-up",
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
                    // Insert Url, and Method Here
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