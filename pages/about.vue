<template>
    <div>
        <h2>About</h2>
        <p>Learn more about The Long Weekend Pizza</p>
        <div class="column-2">
            <div class="w-1/2 m-2 p-2 ">
                <img src="/chef-in-action.png" class="w-full rounded-lg h-lvh h-">
            </div>
            <div class="w-1/2 m-2 p-2 ml-auto">
            </div>
        </div>
    </div>

    <div>
        <slot />
    </div>
</template>


<script setup>
    definePageMeta({
        layout: 'default',
    })
</script>


<style scoped>
h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

p {
    margin: 0px 0;
}


</style>