<template>
    <div class="text-white text-3xl w-full flex flex-col flex-wrap align-center px-5 my-10">
        <img src="stroopwafel-solid.svg" class="h-20 invert mb-10">
      <span class="leading-snug">"Good design is obvious;</span>
      <span class="mb-4 ml-3 leading-snug"><strong>Great design is transparent."</strong></span>
      <span class="text-xl ml-3">-JOE SPARANO</span>
    </div>
</template>

<style scoped>
img{
    animation: spin 20s linear 0s infinite;
}

@keyframes spin {
    0% {transform: rotate(0deg);}
    100% {transform: rotate(360deg);}
}
</style>