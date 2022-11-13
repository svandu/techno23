<template>
  <div class="nav-bar">
    <div class="nav-content">
      <p class="logo">Technorollix'23</p>
      <div class="hambar" @click="toggleMenu">
        <svg
          version="1.0"
          xmlns="http://www.w3.org/2000/svg"
          width="50px"
          height="50px"
          viewBox="0 0 64.000000 64.000000"
          preserveAspectRatio="xMidYMid meet"
        >
          <g
            transform="translate(0.000000,64.000000) scale(0.100000,-0.100000)"
            fill="#ffffff"
            stroke="none"
          >
            <path
              d="M45 509 c-4 -6 -3 -15 2 -20 5 -5 122 -8 279 -7 231 3 269 5 269 18
0 13 -38 15 -272 18 -190 2 -274 -1 -278 -9z"
            />
            <path
              d="M45 329 c-16 -25 20 -29 241 -27 196 3 229 5 229 18 0 13 -34 15
-232 18 -161 2 -234 -1 -238 -9z"
            />
            <path
              d="M45 149 c-15 -24 17 -29 151 -27 116 3 139 6 139 18 0 12 -24 15
-142 18 -96 2 -144 -1 -148 -9z"
            />
          </g>
        </svg>
      </div>
      <div class="nav-menu" v-show="showMenu">
        <div class="cancel" @click="toggleMenu">
          <svg
            version="1.0"
            xmlns="http://www.w3.org/2000/svg"
            width="50px"
            height="50px"
            viewBox="0 0 64.000000 64.000000"
            preserveAspectRatio="xMidYMid meet"
          >
            <g
              transform="translate(0.000000,64.000000) scale(0.100000,-0.100000)"
              fill="#ffffff"
              stroke="none"
            >
              <path
                d="M223 622 c-109 -39 -178 -112 -210 -221 -29 -102 4 -228 82 -306 122
-121 328 -121 450 0 91 92 118 241 64 356 -69 146 -241 223 -386 171z m212
-46 c221 -102 221 -410 0 -512 -36 -17 -68 -24 -115 -24 -158 0 -280 122 -280
280 0 158 122 280 280 280 47 0 79 -7 115 -24z"
              />
              <path
                d="M180 448 c0 -7 26 -38 57 -70 l57 -58 -57 -58 c-31 -32 -57 -63 -57
-70 0 -25 26 -10 82 45 l58 57 58 -57 c32 -31 63 -57 70 -57 25 0 10 26 -45
82 l-57 58 57 58 c31 32 57 63 57 70 0 25 -26 10 -82 -45 l-58 -57 -58 57
c-56 55 -82 70 -82 45z"
              />
            </g>
          </svg>
        </div>
        <div class="menu-links">
          <nuxt-link to="/">Events</nuxt-link>
          <nuxt-link to="/">Schedule</nuxt-link>
          <nuxt-link to="/">Team</nuxt-link>
          <nuxt-link to="/">Gallery</nuxt-link>
          <nuxt-link to="/">About us</nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showMenu: false,
    }
  },

  methods: {
    toggleMenu() {
      this.showMenu = !this.showMenu
    },
  },
}
</script>

<style lang="scss" scoped>
.nav-bar {
  position: absolute;
  width: 100%;
  top: 0;
  z-index: 1;

  .nav-content {
    display: flex;
    position: relative;
    padding: 1.5em 5%;

    .logo {
      font-size: 1.4rem;
      font-family: 'Kaushan Script', cursive;
      color: #fff;
    }

    .hambar {
      position: absolute;
      right: 5%;
      cursor: pointer;
    }

    .nav-menu {
      position: absolute;
      top: 0;
      right: 0;
      height: 100vh;
      width: 70%;

      .cancel {
        position: absolute;
        top: 50%;
        left: -8%;
        transform: translate(-8%, -50%);

        svg {
          transition: rotate 400ms ease-out;
          &:hover {
            cursor: pointer;
            rotate: 360deg;
          }
        }
      }

      .menu-links {
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        background: #e3b5a4;

        a {
          margin: 4rem 3rem 1rem 0;
          list-style: none;
          text-decoration: none;
          font-size: 1.2rem;
          color: #000;
          font-family: 'Poppins', sans-serif;
          font-size: 3rem;
          font-weight: 600;
          letter-spacing: 0.1rem;
          position: relative;
          width: fit-content;

          &::before {
            content: '';
            position: absolute;
            bottom: 23%;
            left: -16%;
            display: block;
            background: #000;
            border-radius: 50%;
            height: 20px;
            width: 20px;
            opacity: 0;
            transition: opacity 500ms ease-in-out;
          }

          &:hover::before {
            opacity: 1;
          }
        }
      }
    }
  }
}
</style>