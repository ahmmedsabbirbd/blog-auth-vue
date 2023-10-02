//create home component
<script setup>
// import { authStore } from '../store/store';
import { authStore } from '../store/piniastore';
const auth = authStore()
</script>
<template>
    <h1 class="text-2xl mb-3">This is Login page</h1>
    <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam doloremque natus eligendi. Dicta ullam obcaecati quidem blanditiis, illum minus possimus earum adipisci sunt accusantium autem. Saepe molestias quaerat enim. Autem.
    </p>

    <p class="mt-10">
        <button @click="auth.authenticate()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
            <span v-if="auth.isAuthenticated">You're already logged in</span>
            <span v-else>Click to Login</span>
        </button>

        <button @click="auth.logout()" class="ml-5 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
            Log out
        </button>
    </p>
</template>

<style></style>