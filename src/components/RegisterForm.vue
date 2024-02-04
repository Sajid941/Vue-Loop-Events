<script setup>
import {reactive} from "vue"

const userdata = reactive({
        username:"",
        useremail:"",
        userpassword:"",
        userconfirm:""
})
function register(){
        if(userdata.userpassword == userdata.userconfirm){
                console.log(userdata)
        }
        else{
                alert("password not match");
        }
}
</script>
<template>
        <!-- component -->
        <!-- Create by joker banny -->
        <div class="h-screen bg-indigo-100 flex justify-center items-center">
                <div class="lg:w-2/5 md:w-1/2 w-2/3">
                        <form class="bg-white p-10 rounded-lg shadow-lg min-w-full">
                                <h1 class="text-center text-2xl mb-6 text-gray-600 font-bold font-sans">Formregister</h1>
                                <div>
                                        <label class="text-gray-800 font-semibold block my-3 text-md"
                                                for="username">Username</label>
                                        <input v-model="userdata.username" class="w-full bg-gray-100 px-4 py-2 rounded-lg focus:outline-none" type="text"
                                                name="username" id="username" placeholder="username" />
                                </div>
                                <div>
                                        <label class="text-gray-800 font-semibold block my-3 text-md" for="email">Email</label>
                                        <input v-model="userdata.useremail" class="w-full bg-gray-100 px-4 py-2 rounded-lg focus:outline-none" type="text"
                                                name="email" id="email" placeholder="@email" />
                                </div>
                                <div>
                                        <label class="text-gray-800 font-semibold block my-3 text-md"
                                                for="password">Password</label>
                                        <input  v-model="userdata.userpassword" class="w-full bg-gray-100 px-4 py-2 rounded-lg focus:outline-none" type="text"
                                                name="password" id="password" placeholder="password" />
                                </div>
                                <div>
                                        <label class="text-gray-800 font-semibold block my-3 text-md" for="confirm">Confirm
                                                password</label>
                                        <input  v-model="userdata.userconfirm" class="w-full bg-gray-100 px-4 py-2 rounded-lg focus:outline-none" type="text"
                                                name="confirm" id="confirm" placeholder="confirm password" />
                                </div>
                        <button @click.prevent="register" type="submit"
                                class="w-full mt-6 bg-indigo-600 rounded-lg px-4 py-2 text-lg text-white tracking-wide font-semibold font-sans">Register</button>
                </form>
        </div>
</div></template>