<template>
    <button>LoginButton</button>
</template>

<script>
    import Vue from 'vue'
    export default {
        name : 'loginbutton',
        data() {
            return {
                loginUrl = `${env.oneauthURL}/oauth/authorize?response_type=code&client_id=${env.clientId}&redirect_uri=${env.publicUrl}`
            }
        },
        methods : {
            logIn () {
                window.location.href = this.loginUrl
            }
            logOut () {

            }
        }
    }
</script>
