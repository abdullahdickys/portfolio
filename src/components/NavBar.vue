<script>
export default {
  name: "NavBar",
  data() {
    return {
      showMenu: false,
    };
  },
  methods: {
    toggleNavbar: function () {
      this.showMenu = !this.showMenu;
    },
  },
};
</script>

<template>
  <div>
    <nav
      class="
        fixed-top
        z-10
        mx-auto
        inset-x-0
        top-0
        relative
        flex-wrap
        items-center
        justify-between
        px-2
        py-3
      "
    >
      <div
        class="
          container
          px-4
          mx-auto
          flex flex-wrap
          items-center
          justify-between
        "
      >
        <div
          class="
            w-full
            relative
            flex
            justify-between
            lg:w-auto
            px-4
            lg:static lg:block lg:justify-start
          "
        >
          <a
            class="
              text-sm
              font-semibold
              leading-relaxed
              inline-block
              mr-4
              py-2
              whitespace-nowrap
            "
          >
            LOGO
          </a>
          <button
            class="
              cursor-pointer
              text-xl
              leading-none
              px-3
              py-1
              border border-solid border-transparent
              rounded
              bg-transparent
              block
              lg:hidden
              outline-none
              focus:outline-none
            "
            type="button"
            v-on:click="toggleNavbar()"
          >
            <i class="fas fa-bars"></i>
          </button>
        </div>
        <div
          v-bind:class="{ hidden: !showMenu, flex: showMenu }"
          class="lg:flex lg:flex-grow items-center"
        >
          <ul class="flex flex-col lg:flex-row list-none ml-auto active">
            <li class="nav-item">
              <a
                class="
                  px-3
                  py-2
                  flex
                  items-center
                  text-sm
                  font-semibold
                  leading-snug
                  hover:opacity-75
                "
              >
                <router-link to="/">Home</router-link>
              </a>
            </li>
            <li class="nav-item">
              <a
                class="
                  px-3
                  py-2
                  flex
                  items-center
                  text-sm
                  font-semibold
                  leading-snug
                  hover:opacity-75
                "
              >
                <router-link to="blog">Work</router-link>
              </a>
            </li>
            <li class="nav-item">
              <a
                class="
                  px-3
                  py-2
                  flex
                  items-center
                  text-sm
                  font-semibold
                  leading-snug
                  hover:opacity-75
                "
              >
                <router-link to="about">About</router-link>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

<style scope>
/* .border-b {
  align-content: center;
  padding: 20px;
  text-align: center;
}

.border-b a {
  font-weight: bold;
  padding: 7px;
  color: #2c3e50;
}

.border-b a.router-link-exact-active {
  color: #42b983;
} */
.fixed-top {
  position: fixed;
  top: 0;
  width: 100%;
  background: rgba(255, 255, 255, 0.5);

  backdrop-filter: blur(20px);
}
.active {
  color: #2c3e50;
}
.active a.router-link-exact-active {
  color: #556ce5;
  font-weight: bold;
  /* padding: 7px; */
  border-bottom-width: 5px;
  padding-bottom: 5px;
}
</style>
