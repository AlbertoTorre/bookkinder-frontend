<template>
    <div class="flex flex-col min-h-screen font-sans">
        <!-- Header -->
        <header class="bg-blue-800 text-white px-6 py-4 flex justify-between items-center">
            <h1 class="text-xl font-bold">📚 Book System</h1>
            <nav class="space-x-4">
                <NuxtLink to="/" class="hover:underline">Home</NuxtLink>
                <NuxtLink to="/books" class="hover:underline">Books</NuxtLink>
                <NuxtLink to="/users" class="hover:underline">Users</NuxtLink>
            </nav>
        </header>

        <!-- Main Content -->
        <main class="flex-1 px-6 py-8 bg-gray-100">
            <slot />
        </main>

        <!-- Footer -->
        <footer class="bg-blue-800 text-white text-center py-4">
            &copy; {{ new Date().getFullYear() }} Book System
        </footer>
    </div>
</template>
