<template>
    <div class="max-w-6xl mx-auto border-2 border-gray-300 rounded-lg shadow-md mb-4">
      <div @click="toggleOpen" class="flex justify-between items-center cursor-pointer bg-white rounded-t-lg p-4">
        <h2 class="text-2xl font-bold text-center text-gray-800 w-full">{{ title }}</h2>
        <svg v-if="!isOpen" class="w-4 h-4 transform rotate-90 text-gray-600" fill="none" stroke="currentColor"
             viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path>
        </svg>
        <svg v-else class="w-4 h-4 text-gray-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"
             xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 10l7-7 7 7M5 19l7-7 7 7">
          </path>
        </svg>
      </div>
      <div v-if="isOpen" class="bg-gray-100 rounded-b-lg p-4">
        <div v-html="content"></div>
        <button class="mt-6 bg-gray-200 px-3 py-1 rounded-lg text-lg">Clôture de l'entrée {{ entryNumber }}</button>
      </div>
    </div>
  </template>

<script>
export default {
    props: {
        title: {
            type: String,
            required: true
        },
        content: {
            type: String,
            required: true
        },
        entryNumber: {
            type: Number,
            required: true
        }
    },
    data() {
        return {
            isOpen: false
        }
    },
    methods: {
        toggleOpen() {
            this.isOpen = !this.isOpen;
        },
    }
}
</script>