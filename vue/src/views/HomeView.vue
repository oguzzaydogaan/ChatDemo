<script setup lang="ts">
import { RouterLink } from 'vue-router'
import { ref } from 'vue'
const uid = ref('')
</script>

<template>
  <main
    class="flex justify-center items-center h-screen px-3 xl:px-[400px] lg:px-[300px] md:px-[200px] sm:px-[100px]"
  >
    <div
      class="bg-white grid grid-cols-1 w-full shodow-lg rounded-lg p-5 px-8 xl:px-20 lg:px-16 md:px-8 sm:px-12"
    >
      <h4 class="text-center text-2xl text-gray-700 font-semibold">Sign in</h4>
      <input
        v-model="uid"
        class="text-gray-600 placeholder-gray-600 bg-gray-200 rounded-full text-center p-1 mt-5 mx-7"
        type="text"
        placeholder="User.Id"
      />

      <RouterLink
        class="bg-blue-500 text-white rounded-full mx-28 p-1 mt-2 text-center"
        :to="`${uid}/chats`"
        >Sign in</RouterLink
      >
    </div>
  </main>
</template>
