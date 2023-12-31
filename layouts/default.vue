<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 flex justify-between">
            <NuxtLink to="/" class="font-bold"><img src="/logo.jpg" class="min-h-10 md:max-h-10"></NuxtLink>
                <ul class="flex gap-4">
                    <li>
                        <NuxtLink to="/">Home</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/about">About</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/menu">Menu</NuxtLink>
                    </li>
                </ul>
            <button class="text-white bg-gradient-to-r from-cyan-400 via-cyan-500 to-cyan-600 hover:bg-gradient-to-br focus:ring-4 focus:outline-none focus:ring-cyan-300 dark:focus:ring-cyan-800 font-medium rounded-lg text-sm px-5 py-2.5 text-center me-2 mb-2 px-4 py-2 rounded">Order Now!</button>

            </nav>
        </header>

<!-- Output Page Content -->
        <div class="container mx-auto p-4">
            <slot />
        </div>
    </div>

</template>


<style scoped>
    .router-link-exact-active {
        color: #84b3d9;
    }
</style>
