<template>
  <div id="experience">
    <p class="text-3xl text-center md:py-16 py-8 pb-5 font-bold">
      WORK EXPERIENCE
    </p>
    <div v-for="(item, index) in projects" :key="index">
      <div class="md:flex" :class="{ 'flex-row-reverse': index % 2 !== 0 }">
        <div
          class="flex items-center justify-center w-full md:w-1/2"
          :class="{
            'border-b border-[#286dab] md:border-b-0':
              index != projects.length - 1,
          }"
        >
          <div class="lg:px-16 px-8 py-4">
            <p v-html="item.content"></p>
          </div>
        </div>
        <div
          class="relative overflow-hidden -z-10 md:block hidden"
          :class="{ 'right-5': index % 2 === 0 }"
        >
          <div class="circle"></div>
          <div class="line"></div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      projects: [
        {
          content: `<div>
            <p class="text-xl font-bold">
              Member Of Technical Staff - 1 (Blowhorn)
            </p>
            <p class="italic text-teal-500 ">04/2022 - 12/2023,</p>
            <p class="italic text-teal-500">Achievements/Tasks</p>
            <ul style="list-style-type:disc" class="text-lg">
              <li class="py-1">
                Migrated and developed a new design for an existing UI of a product to look more user-friendly and attractive, which resulted in increased demand by 40% by existing and new clients in the market.
              </li>
              <li class="py-1">
                Contributed to project architecture to improve the development
                process and remove the dependency between teams, so everyone can
                work parallel without depending on each other.
              </li>
              <li class="py-1">
                Developed Routes Conﬁguration & ﬂeet overview module with Google
                Map, Marker and Google Autocomplete from scratch which assigns
                routes to the drivers for delivering products and to list the
                available ﬂeet in selected location, hub, vehicle type and
                driver name.
              </li>
              <li class="py-1">
                Developed a Popup with a Scanner that advertises Users to download Integrated Fulfillment Mobile App which further boosted the app download by 60%.
              </li>
              <li class="py-1">
                Developed Wallet module with razorPay and paytm payment gateway
                integration. where user can add money to their wallet using
                multiple payment gateway options, and also can view the credit
                and debit amount along with multiple details.
              </li>
              <li class="py-1">
                Building the Whatsapp Notification, Delivery serviceability, and Contact Us feature in the Blowhorn Website and handling multiple API Integrations.
              </li>
              <li class="py-1">
                Trouble shooting 70% of bugs in the Integrated Fulfillment Platform.
              </li>
              <li class="py-1 font-semibold">
                Tech Stack:- HTML5, CSS3, Javascript, Vue Js , Nuxt js, Tailwind
                css, PrimeVue.
              </li>
            </ul>
            </div>`,
          id: 1,
        },
        {
          content: `<div>
            <p class="text-xl font-bold">
              Full-Stack Web Development (Training) (Masai School)
            </p>
            <p class="italic text-teal-500 ">07/2021 - 03/2022,</p>
            <p class="italic text-teal-500">Achievements/Tasks</p>
            <ul style="list-style-type:disc" class="text-lg">
              <li class="py-1">
                Learned Full Stack Web Development and assisted other students and evaluated their codes.
              </li>
              <li class="py-1">
                Created Upgrad Clone web application.
              </li>
              <li class="py-1">
                Built authentication and integrated it with the front end.
              </li>
              <li class="py-1">
                Laid out the database schema and build the REST API for the same.
              </li>
              <li class="py-1">
                Understood the concepts of React, hooks API calling, and Redux by creating the Meesho Clone website.
              </li>
              <li class="py-1 font-semibold">
                Tech Stack:- HTML5, CSS3, JavaScript, React Js, Redux, Node Js, Express Js, Mongo DB, Material UI 
              </li>
            </ul>
            </div>`,
          id: 2,
        },
      ],
    };
  },
};
</script>
<style scoped>
.circle {
  background-color: rgb(255, 255, 255);
  border: 3px solid gray;
  border-radius: 100%;
  width: 20px; /* +6 for border */
  height: 20px;
}
.line {
  top: 20px;
  left: 9px;
  height: 100%;
  position: absolute;
  border-left: 3px solid gray;
}
</style>
