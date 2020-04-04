<template>
    <div class="container mt-16">
        <a href="" @click.prevent="submit">Sign in</a>
    </div>
</template>

<script>
export default {
    methods: {
        async submit() {
            this.$auth.loginWith('local', {
                data: {
                    email: 'joe@doe.com',
                    password: 'password'
                }
            })
        }
    }
}
</script>