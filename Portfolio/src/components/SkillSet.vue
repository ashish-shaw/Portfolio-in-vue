<template>
  <div id="skills" class="bg-[#f2f2f2] md:py-16 py-8">
    <p class="text-3xl text-center pb-5 font-bold">Skills & Interests</p>
    <div class=" ">
      <div class="max-w-[1100px] flex flex-wrap justify-evenly m-auto">
        <div
          v-for="(item, index) in skillLists"
          :key="index"
          class="h-[140px] w-[140px] bg-white p-5 shadow-xl m-5 flex justify-center items-center rounded-xl border cursor-pointer hover:scale-110 duration-300"
        >
          <div>
            <img
              class="w-[80px] h-[80px] flex justify-center"
              :src="item.url"
              :alt="item.name"
            />
            <p class="font-light text-center">{{ item.name }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      skillLists: [
        {
          name: "Html5",
          url: require("../assets/skills/html.svg"),
        },
        {
          name: "CSS3",
          url: require("../assets/skills/css.svg"),
        },
        {
          name: "JavaScript",
          url: require("../assets/skills/javascript.svg"),
        },
        {
          name: "VueJs",
          url: require("../assets/skills/vue.svg"),
        },
        {
          name: "NuxtJs",
          url: require("../assets/skills/nuxt.svg"),
        },
        {
          name: "Tailwind CSS",
          url: require("../assets/skills/tailwind.svg"),
        },
        {
          name: "Prime Vue",
          url: require("../assets/skills/primeVue.png"),
        },
        {
          name: "React",
          url: require("../assets/skills/react.svg"),
        },
        {
          name: "Redux",
          url: require("../assets/skills/redux.svg"),
        },
        // {
        //   name: "Knockout Js",
        //   url: require("../assets/skills/knockoutJs.png"),
        // },
        {
          name: "Algorithms",
          url: require("../assets/skills/algorithm.svg"),
        },
        {
          name: "Bootstrap",
          url: require("../assets/skills/bootstrap.svg"),
        },
        {
          name: "Github",
          url: require("../assets/skills/github.svg"),
        },
      ],
    };
  },
};
</script>
<style scoped>

</style>
