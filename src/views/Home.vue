<script>
import { defineComponent } from "vue";
import ButtonRepo from "@/components/ButtonRepo.vue";
// import TypeEffect from "@/components/TypeEffect.vue";

export default defineComponent({
  components: { ButtonRepo },
});
</script>

<template>
  <div class="bg-gray-50 pt-6">
    <div class="hero container max-w-screen-lg mx-auto pb-12 mx-auto">
      <div
        class="h-64 rounded-md overflow-hidden bg-cover bg-center mx-auto"
        style="
          background-image: url('https://images.pexels.com/photos/57690/pexels-photo-57690.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940');
          height: 450px;
        "
      >
        <div
          class="
            bg-gray-900 bg-opacity-50
            flex
            items-center
            place-self-center
            h-full
          "
        >
          <div class="px-10 md:py-8">
            <div class="flex flex-wrap justify-center">
              <div class="w-6/12 sm:w-4/12 px-12 w-25 h-25 object-cover">
                <img
                  src="https://www.creative-tim.com/learning-lab/tailwind-starter-kit/img/team-4-470x470.png"
                  alt="..."
                  class="
                    shadow-lg
                    rounded-full
                    max-w-full
                    h-auto
                    align-middle
                    border-none
                  "
                />
              </div>
            </div>
            <h2 class="text-2xl text-white font-bold text-center mt-2">
              Abdullah Dicky Syarifuddin
            </h2>

            <p class="mt-2 text-white font-semibold text-center">
              Adobe Illustrator | Corel Draw | Adobe Photoshop | Laravel | Vue
              js.
            </p>
            <button
              class="
                flex
                items-center
                mt-4
                px-3
                py-2
                text-white text-sm
                font-medium
                rounded
                hover:bg-blue-500
                focus:outline-none focus:bg-blue-500
                mx-auto
                font-semibold
                btn-gra
              "
              id="btn-gra"
            >
              <router-link to="blog">Get Started</router-link>
              <svg
                class="h-5 w-5 mx-2"
                fill="none"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path d="M17 8l4 4m0 0l-4 4m4-4H3"></path>
              </svg>
            </button>
          </div>
        </div>
      </div>
      <div
        class="
          max-w-screen-xl
          px-4
          py-12
          mx-auto
          sm:px-6
          lg:py-16 lg:px-8 lg:flex lg:items-center lg:justify-between
        "
      >
        <h2
          class="
            text-3xl
            font-extrabold
            leading-9
            tracking-tight
            text-gray-900
            sm:text-4xl sm:leading-10
          "
        >
          Ready to dive in?
          <br />
          <span class="text-indigo-600">Vite 2.x + Vue 3.x + Tailwind 2.x</span>
        </h2>
        <div class="flex mt-8 lg:flex-shrink-0 lg:mt-0">
          <div class="inline-flex rounded-md shadow">
            <router-link
              to="/blog"
              class="
                inline-flex
                items-center
                justify-center
                px-5
                py-3
                text-base
                font-medium
                leading-6
                text-white
                transition
                duration-150
                ease-in-out
                bg-indigo-600
                border border-transparent
                rounded-md
                hover:bg-indigo-500
                focus:outline-none
              "
              >Next Page</router-link
            >
          </div>
          <ButtonRepo />
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
#btn-gra {
  top: 50%;
  left: 50%;
  height: 60px;
  width: 170px;
  transform: transfer(-50%, -50%);
  text-align: center;
  text-decoration: none;
  line-height: 60px;
  color: #fff;
  text-transform: uppercase;
  box-sizing: border-box;
  background: linear-gradient(90deg, #03a9f4, #f441a5, #ffeb3b, #03a9f4);
  background-size: 400%;
  padding-bottom: 7px;
}

#btn-gra:hover {
  color: #fff;
  text-decoration: none;
  animation: animate 8s linear infinite;
}

@keyframes animate {
  0% {
    background-position: 0%;
  }
  100% {
    background-position: 400%;
  }
}

#btn-gra:before {
  content: "";
  top: -5px;
  left: -5px;
  bottom: -5px;
  right: -5px;
  z-index: -1;
  background: linear-gradient(90deg, #03a9f4, #f441a5, #ffeb3b, #03a9f4);
  background-size: 400%;
  border-radius: 40px;
  filter: blur(20px);
  opacity: 0;
  transition: 0.5s;
}

#btn-gra:hover:before {
  filter: blur(20px);
  opacity: 1;
  animation: animate 8s linear infinite;
}
</style>
