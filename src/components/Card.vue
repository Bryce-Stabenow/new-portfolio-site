<template>
    <div 
        class="w-full p-5 mb-4 rounded-2xl text-white"
        :class="[expanded ? 'bg-gray-600 shadow-xl' : 'shadow-lg bg-gray-700']"
        @click="toggle"
    >
    <div class="w-full flex flex-row justify-between items-center mb-2"> 
        <h1 class="text-3xl font-bold" style="color: #00eeff;">{{ cardTitle }}</h1>
        <img 
            src="chevron-down.svg" 
            class="h-5 invert cursor-pointer duration-100"
            :class="[expanded ? 'rotate-180' : '']"
            >
    </div>
        <p 
            v-if="contactMe===false"
            class="text-justify"
            :class="{ hidden: !expanded}"
        >{{ description }}</p>
        <ul 
            v-else
            :class="{ hidden: !expanded}"
        >If you want to get in touch...
            <li class="mt-4">Tweet me <a href="https://www.twitter.com/BryceStabenow" target="_blank" rel="noopener noreferrer">@BryceStabneow</a></li>
            <li><a href="mailto: brycestabenow617@gmail.com">Email me</a></li>
            <li>Send a raven to <a href="https://www.youtube.com/watch?v=SkWbkcm0WA8" target="_blank" rel="noopener noreferrer">Winterfell</a></li>
        </ul>
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
        },
        contactMe: {
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
ul{
    list-style: circle inside;
}
a{
    text-decoration: underline;
    font-weight: bold;
}
a:hover{
    cursor: pointer;
}
</style>