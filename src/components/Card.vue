<template>
    <div 
        class="w-full p-5 bg-gray-700 mb-4 rounded-2xl cursor-pointer shadow-xl text-white"
        :class="{ expanded : expanded }"
        @click="toggle"
    >
    <div class="w-full flex flex-row justify-between items-center  mb-2"> 
        <h1 class="text-3xl">{{ cardTitle }}</h1>
        <img src="chevron-down.svg" class="h-5">
    </div>
        <p 
            class="text-justify"
            :class="{ hidden: !expanded}"
        >{{ description }}</p>
    </div>
</template>

<script>
export default {
    props: {
        cardTitle: String,
        description: String,
        open: {
            type: Boolean,
            default: false,
        }
    },

    data() {
        return {
            expanded: this.open,
        };
    },

    methods: {
        toggle(){
            this.expanded = !this.expanded;
        }
    },
}
</script>

<style scoped>
.expanded{
    height: 300px;
}
</style>