<script>
export default {
  data() {
    return {
      works: [
        {
          id: "0",
          img: "require(`@/assets/cawang-01.jpg`)",
          tag: "#Logo",
          link: ""
        },
        {
          id: "1",
          img: "require(`@/assets/abstract.jpg`)",
          tag: "#Illustration",
          link: ""
        },
        {
          id: "2",
          img: "require(`@/assets/fingerprint-text.png`)",
          tag: "#Photoshop",
          link: ""
        },
        {
          id: "3",
          img: "require(`@/assets/pattern-2.png`)",
          tag: "#Pattern",
          link: ""
        },
        {
          id: "4",
          img: "require(`@/assets/pattern-japan.png`)",
          tag: "#Typograph",
          link: ""
        },
      ],
    };
  },

  methods: {
    myFunction: function () {
      window.open("https://www.google.com", "_blank");
    },
  },
};
</script>
<template>
  <div>
    <main
      class="
        grid
        place-items-center
        min-h-screen
        bg-gradient-to-t
        from-blue-200
        to-indigo-900
        p-5
      "
    >
      <div>
        <h1
          class="text-4xl sm:text-5xl md:text-7xl font-bold text-gray-200 mb-5"
        >
          Made for you
        </h1>
        <section class="grid grid-cols-1 sm:grid-cols-3 gap-4">
          <!-- CARD 1 -->
          <div
            class="bg-gray-900 shadow-lg rounded p-3"
            v-for="work in works"
            :key="work.id"
          >
            <div class="group relative">
              <img
                :src="works.img"
                class="w-full md:w-72 block rounded"
                alt=""
              />
              <div
                class="
                  absolute
                  bg-black
                  rounded
                  bg-opacity-0
                  group-hover:bg-opacity-60
                  w-full
                  h-full
                  top-0
                  flex
                  items-center
                  group-hover:opacity-100
                  transition
                  justify-evenly
                "
              >
                <button
                  class="
                    hover:scale-110
                    text-white
                    opacity-0
                    transform
                    translate-y-3
                    group-hover:translate-y-0 group-hover:opacity-100
                    transition
                  "
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="23"
                    height="23"
                    fill="currentColor"
                    viewBox="0 0 24 24"
                  >
                    <path
                      fill="#FFFFFF"
                      d="M21,14a1,1,0,0,0-1,1v4a1,1,0,0,1-1,1H5a1,1,0,0,1-1-1V15a1,1,0,0,0-2,0v4a3,3,0,0,0,3,3H19a3,3,0,0,0,3-3V15A1,1,0,0,0,21,14Zm-9.71,1.71a1,1,0,0,0,.33.21.94.94,0,0,0,.76,0,1,1,0,0,0,.33-.21l4-4a1,1,0,0,0-1.42-1.42L13,12.59V3a1,1,0,0,0-2,0v9.59l-2.29-2.3a1,1,0,1,0-1.42,1.42Z"
                    />
                  </svg>
                </button>
                <button
                  @click="myFunction()"
                  class="
                    hover:scale-110
                    text-white
                    opacity-0
                    transform
                    translate-y-3
                    group-hover:translate-y-0 group-hover:opacity-100
                    transition
                  "
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="30"
                    height="30"
                    viewBox="0 0 24 24"
                  >
                    <path
                      fill="#FFFFFF"
                      d="M15,10H12V7a1,1,0,0,0-2,0v3H7a1,1,0,0,0,0,2h3v3a1,1,0,0,0,2,0V12h3a1,1,0,0,0,0-2Zm6.71,10.29L18,16.61A9,9,0,1,0,16.61,18l3.68,3.68a1,1,0,0,0,1.42,0A1,1,0,0,0,21.71,20.29ZM11,18a7,7,0,1,1,7-7A7,7,0,0,1,11,18Z"
                    />
                  </svg>
                </button>

                <button
                  class="
                    hover:scale-110
                    text-white
                    opacity-0
                    transform
                    translate-y-3
                    group-hover:translate-y-0 group-hover:opacity-100
                    transition
                  "
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="20"
                    height="20"
                    fill="currentColor"
                    class="bi bi-three-dots"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M3 9.5a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3zm5 0a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3zm5 0a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3z"
                    />
                  </svg>
                </button>
              </div>
            </div>
            <div class="p-5">
              <h3 class="text-white text-lg">{{work.tag}}</h3>
              <p class="text-gray-400">Tycho</p>
            </div>
          </div>
          <!-- END OF CARD 1 -->
        </section>
      </div>
    </main>
  </div>
</template>
