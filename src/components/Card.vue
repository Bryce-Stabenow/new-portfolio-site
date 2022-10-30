<template>
    <div class="w-full p-5 bg-gray-700 rounded-2xl text-center mb-10 cursor-pointer h-96 shadow-xl hover:bg-gray-600 hover:scale-105"
    >
        <h1 class="text-white text-3xl">{{cardTitle}}</h1>
    </div>
</template>

<script>
export default {
    setup() {
        
    },

    props: ['card-title', 'description'],
}
</script>
