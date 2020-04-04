<template>
    <div class="container mt-16">
        <div class="flex flex-col items-center">
        <h1 class="text-3xl text-gray-700 font-medium">Sign In</h1>

            {{ form }}
            <form 
                @submit.prevent="submit"
                action="#" 
                class="bg-white p-8 rounded w-full mb-6">
                <div class="mb-6">
                    <label for="email" class="block text-gray-600 font-medium mb-2">
                        Email
                    </label>
                    <input 
                        class="border-2 border-gray-400 rounded block w-full p-3"
                        type="text" 
                        name="email"
                        id="email"
                        v-model="form.email"
                        >
                </div>
                <div class="mb-6">
                    <label for="password" class="block text-gray-600 font-medium mb-2">
                        Password
                    </label>
                    <input 
                        class="border-2 border-gray-400 rounded block w-full p-3"
                        type="password" 
                        name="password"
                        id="password"
                        v-model="form.password"
                        >
                </div>

                <button 
                    type="submit" 
                    class="bg-blue-500 text-white p-4 rounded text-center font-medium block w-full">
                Submit</button>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            form: {
                email: '',
                password: ''
            }
        }
    },
    methods: {
        async submit() {
            this.$auth.loginWith('local', {
                data: this.form
            })
        }
    }
}
</script>