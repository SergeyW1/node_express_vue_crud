<script setup lang="ts">
import {usePostStore} from "@/stores/postStore";

const postStore = usePostStore()

postStore.getPosts()
</script>

<template>
   <nav class="bg-white shadow dark:bg-gray-800">
      <div class="container flex items-center justify-center p-6 mx-auto text-gray-600 capitalize dark:text-gray-300">
         <router-link :to="{name: 'posts'}"
                      class="text-gray-800 dark:text-gray-200 border-blue-500 mx-1.5 sm:mx-6"
                      active-class="active-link"
         >
            Posts
         </router-link>

         <router-link :to="{name: 'create'}"
                      class="text-gray-800 dark:text-gray-200 border-blue-500 mx-1.5 sm:mx-6"
                      active-class="active-link"
         >
            Add Post
         </router-link>
      </div>
   </nav>
   <router-view/>
</template>

<style scoped lang="postcss">
.active-link {
   @apply border-b-2
}
</style>
