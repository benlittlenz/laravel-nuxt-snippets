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
                   <li class="">
                    <nuxt-link 
                        :to="{name: 'home'} "
                        class="text-lg text-gray-700 py-8 px-4"
                    >Sign In</nuxt-link>
                   </li> 

                   <li class="">
                    <nuxt-link 
                        :to="{name: 'home'} "
                        class="text-lg text-gray-700 py-8 px-4"
                    >Create Account</nuxt-link>
                   </li> 

                   <li class="">
                    <nuxt-link 
                        :to="{name: 'home'} "
                        class="text-lg text-gray-700 py-8 px-4"
                    >Sign Out</nuxt-link>
                   </li> 

                   <li class="">
                    <nuxt-link 
                        :to="{name: 'home'} "
                        class="text-lg text-gray-700 py-8 px-4"
                    >User name</nuxt-link>
                   </li> 

                </ul>
            </div>
        </div>
    </div>
</template>