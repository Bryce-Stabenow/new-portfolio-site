<template>
  <div class="h-16 px-4 flex flex-row items-center bg-gray-750 justify-between shadow-xl sticky top-0 z-50">
    <img src="portfolioShot.png" class="h-auto w-10 rounded-full" @click="scrollTop">
    <a class="text-white" href="https://twitter.com/BryceStabenow"><span>Tweet Me!</span></a>
  </div>
</template>

<script>
export default {
  setup() {
    
  },

  methods: {
    scrollTop(){
      console.log('click')
      window.scroll();
    }
  }
}
</script>
