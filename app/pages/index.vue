<script setup lang="ts">
definePageMeta({
    layout: 'default'
})

const { data, error } = await useFetch('/api/hello')
</script>

<template>
    <div class="max-w-2xl mx-auto text-center bg-white shadow-md rounded-md p-6">
        <h1 class="text-2xl font-bold mb-4 text-blue-700">Welcome to Book System</h1>

        <div v-if="error" class="text-red-600">
            <p>Error: {{ error.message }}</p>
        </div>

        <div v-else-if="data" class="text-gray-800">
            <p>{{ data.message }}</p>
        </div>

        <div v-else class="text-gray-500">
            <p>Loading...</p>
        </div>
    </div>
</template>
