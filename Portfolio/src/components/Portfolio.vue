<template>
  <div id="home" class="md:flex justify-evenly md:py-28 py-8 animate">
    <div class="flex justify-center items-center md:pt-0 pt-5">
      <img class="w-[250px] h-[300px] rounded-2xl" src="../assets/profile.jpeg" />
    </div>
    <div class="flex justify-center items-center md:pt-0 pt-5">
      <div class="px-4">
        <p class="text-2xl font-semibold text-center md:text-start">Hi, I am</p>
        <p class="text-[28px] text-[#286dab] font-semibold text-center md:text-start">Ashish Kumar Shaw</p>
        <p class="text-sm font-bold text-[#b37d4e] mt-4">
          Frontend Developer | Competitive programmer
        </p>
        <div class="flex md:block justify-center">
         <div class="mt-4">
          <button
          class="bg-[#286dab] text-sm flex items-center justify-center px-4 py-1 text-white rounded-md hover:scale-110 duration-300 mx-auto md:mx-0"
        >
          <a href="https://drive.google.com/file/d/1jHr8n2WZpsdDgKtCc_fKZJ7DERSPIGUD/view?usp=sharing" type="application/pdf" rel="alternate" media="print" target="_blank">RESUME</a>
        </button>
        <div class="flex space-x-2 mt-4">
          <a
            href="https://github.com/ashish-shaw"
            class="w-12 h-12 flip duration-500"
            ><img src="../assets/git.svg" alt="Github"
          /></a>
          <a href="https://www.linkedin.com/in/ashish-kumar-shaw-9aa7bb214/" class="w-[44px] h-[44px] flip duration-500"
            ><img src="../assets/linkedin.svg" alt="Linkedin"
          /></a>
          <a href="https://twitter.com/Ashish__Shaw" class="w-12 h-12"
            ><img src="../assets/twitter.gif" alt="Twitter"
          /></a>
        </div>
         </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PortFolio",
  data() {
    return {};
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.flip:hover{
   transform: rotateY(360deg);

}
.animate{
  animation-name: slidee;
  animation-duration: 2s;
}
@keyframes slidee{
    from {
        width: 50vw;
        opacity: 0;
    }
    to{
        width: 100vw;
        opacity: none;
        
    }
}
</style>
