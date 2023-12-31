<!-- pages/menu.vue -->
<template>
    <iframe :src="pdfPath" class="w-full aspect-square h-40%"></iframe>
</template>
  
<script>
export default {
    computed: {
        pdfPath() {
            // Adjust the path to your PDF file in the static directory
            return '/menu.pdf';
        },
    },
};
</script>
  

<script setup>
    definePageMeta({
        layout: 'default',
    })
</script>