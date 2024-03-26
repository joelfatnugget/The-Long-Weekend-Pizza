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
                    <li>
                        <NuxtLink to="/order" class="btn">Order</NuxtLink>
                    </li>
                </ul>
            

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
