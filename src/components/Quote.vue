<template>
    <div class="text-white text-3xl w-full flex flex-col flex-wrap align-center px-5 my-10">
        <img src="stroopwafel-solid.svg" class="h-20 invert mb-10">

        <div 
            class="flex flex-col flex-wrap align-center"
            id="scrollbox"
        >
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" fill="#00eeff" height="60" width="60"><!--! Font Awesome Pro 6.2.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M0 216C0 149.7 53.7 96 120 96h8c17.7 0 32 14.3 32 32s-14.3 32-32 32h-8c-30.9 0-56 25.1-56 56v8h64c35.3 0 64 28.7 64 64v64c0 35.3-28.7 64-64 64H64c-35.3 0-64-28.7-64-64V320 288 216zm256 0c0-66.3 53.7-120 120-120h8c17.7 0 32 14.3 32 32s-14.3 32-32 32h-8c-30.9 0-56 25.1-56 56v8h64c35.3 0 64 28.7 64 64v64c0 35.3-28.7 64-64 64H320c-35.3 0-64-28.7-64-64V320 288 216z"/></svg>
            <span class="leading-snug ml-4">Good design is obvious;</span>
            <span class="mb-4 ml-4 leading-snug"><strong>Great design is transparent.</strong></span>
            <span class="text-xl ml-4">-JOE SPARANO</span>
        </div>
    </div>
</template>

<script>
export default{
    data() {
        return {
            fadePos: 0,
        }
    },
    methods: {
        handleScroll() {
            this.fadePos = window.scrollY;
            this.fadeBox();
        },
        fadeBox() {
            document.getElementById('scrollbox').style.opacity = (1000 - this.fadePos * 3) / 1000;
        }
    },
    created() {
        window.addEventListener('scroll', this.handleScroll)
    },
    destroyed() {
        window.removeEventListener('scroll', this.handleScroll)
    }
}
</script>

<style scoped>
img{
    animation: spin 20s linear 0s infinite;
}

@keyframes spin {
    0% {transform: rotate(0deg);}
    100% {transform: rotate(360deg);}
}
</style>