<template>
    <div class="bg-white flex items-center">
        <div class="container flex flex-wrap items-center">
            <nuxt-link 
                :to="{ name: 'home' }"
                class="mr-10"
            >
            Snippets
            </nuxt-link>

            <div class="w-full flex">
                <ul class="h-24 flex items-center">
                   <li class="">
                    <nuxt-link 
                        :to="{name: 'home'} "
                        class="text-lg text-gray-700 py-8 px-4"
                    >Browse</nuxt-link>
                   </li> 
                   <li class="">
                    <nuxt-link 
                        :to="{name: 'home'} "
                        class="text-lg text-gray-700 py-8 px-4"
                    >Search</nuxt-link>
                   </li> 

                </ul>

                <ul class="h-24 flex items-center ml-auto text-right">
                    <template v-if="$auth.loggedIn">
                        <li class="">
                            <nuxt-link 
                                :to="{name: 'home'} "
                                class="text-lg text-gray-700 py-8 px-4"
                            >{{$auth.user.name}}</nuxt-link>
                        </li> 
                            <li class="">
                                <nuxt-link 
                                    :to="{name: 'home'} "
                                    class="text-lg text-gray-700 py-8 px-4"
                                >Dashboard</nuxt-link>
                            </li> 
                            <li class="">
                                <a
                                    href="#"
                                    @click.prevent="signOut"
                                    class="text-lg text-gray-700 py-8 px-4"
                                >Sign Out</a>
                            </li> 
                    </template>
                     <template v-else>
                        <li class="">
                            <nuxt-link 
                                :to="{name: 'auth-signin'} "
                                class="text-lg text-gray-700 py-8 px-4"
                            >Sign In</nuxt-link>
                        </li> 

                        <li class="">
                            <nuxt-link 
                                :to="{name: 'home'} "
                                class="text-lg text-gray-700 py-8 px-4"
                            >Create Account</nuxt-link>
                        </li> 
                    </template>
                   

                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {

        }
    },
    methods: {
        async signOut() {
            await this.$auth.logout()
        }
    }
}
</script>