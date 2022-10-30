<template>
    <div 
        class="w-full p-5 bg-gray-700 rounded-2xl text-center mb-4 cursor-pointer shadow-xl hover:bg-gray-600 hover:scale-105 text-white"
        :class="{ expanded: expanded }"
        @click="toggle"
    >
        <h1 class="text-3xl underline mb-2">{{ cardTitle }}</h1>
        <p 
            class="text-justify"
            :class="{ hidden: !expanded}"
        >{{ description }}</p>
    </div>
</template>

<script>
export default {
    emits: ['closeOthers'],

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
            this.$emit('closeOthers');
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