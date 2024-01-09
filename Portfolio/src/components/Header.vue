<template>
  <div
    class="flex border-b h-16 justify-between sticky top-0 backdrop-blur-sm bg-white/30"
  >
    <a
      href="#home"
      class="pl-6 flex items-center text-[#286dab] no-underline text-[28px] pointer hover:scale-110 duration-300"
      >Ashish Kumar Shaw</a
    >
    <div class="lg:mr-10 md:mr-5 flex space-x-8 items-center">
      <div
        v-for="(item, index) in navList"
        :key="index"
        class="w-auto hidden md:block"
      >
        <a class="navigation" :href="item.url">{{ item.name }}</a>
        <div
          class="border-b-[3px] h-[5px] border-[#42A5F5] duration-300 underlineDiv"
        />
      </div>
      <div class="md:hidden block cursor-pointer pr-4">
        <svg
          @click="toggle"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-6 h-6 relative"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
          />
        </svg>
        <div
          v-if="show"
          class="absolute top-4 right-0 w-[120px] pl-2 bg-[#286dab] py-2 rounded-[4px]"
        >
          <div
            v-for="(item, index) in navList"
            :key="index"
            class="w-auto flex justify-between"
          >
            <div>
              <a class="navigation text-white" :href="item.url">{{
                item.name
              }}</a>
              <div
                class="border-b-[3px] h-[5px] border-[#42A5F5] duration-300 underlineDiv"
              />
            </div>
            <svg
              @click="toggle"
              v-if="index === 0"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-6 h-6 mr-2 text-white"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MyName",
  data() {
    return {
      navList: [
        {
          name: "Home",
          url: "#home",
        },
        {
          name: "About",
          url: "#about",
        },
        {
          name: "Experience",
          url: "#experience",
        },
        {
          name: "Skills",
          url: "#skills",
        },
        {
          name: "Contact",
          url: "#contact",
        },
      ],
      show: false,
    };
  },
  methods: {
    toggle() {
      this.show = !this.show;
    },
  },
};
</script>
<style scoped>
.underlineDiv {
  display: none;
}
.navigation:hover + .underlineDiv {
  display: block;
}
</style>
