<template>
    <div 
        class="w-full p-5 mb-4 rounded-2xl cursor-pointer text-white"
        :class="[expanded ? 'bg-gray-600 shadow-xl' : 'shadow-lg bg-gray-700']"
        @click="toggle"
    >
    <div class="w-full flex flex-row justify-between items-center  mb-2"> 
        <h1 class="text-3xl">{{ cardTitle }}</h1>
        <img 
            src="chevron-down.svg" 
            class="h-5 invert duration-100"
            :class="[expanded ? 'rotate-180' : '']"
            >
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