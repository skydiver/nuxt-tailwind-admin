<template>
  <nav id="header" :class="bgColor" class="fixed w-full z-10 pin-t shadow">
    <div
      class="w-full container mx-auto flex flex-wrap items-center mt-0 pt-3 pb-3 md:pb-0"
    >
      <div class="w-1/2 pl-2 md:pl-0">
        <a
          :class="textColor"
          class=" text-base xl:text-xl no-underline hover:no-underline font-bold"
          href="#"
        >
          <i :class="iconColor" class="fas pr-3"></i> Nuxt.js Admin Starter
        </a>
      </div>
      <div class="w-1/2 pr-0">
        <div class="flex relative inline-block float-right">
          <div :class="textColorAlt" class="relative text-sm">
            <button
              id="userButton"
              class="flex items-center focus:outline-none mr-3"
            >
              <img
                class="w-8 h-8 rounded-full mr-4"
                src="http://i.pravatar.cc/300"
                alt="Avatar of User"
              />
              <span :class="textColorAlt" class="hidden md:inline-block">
                Hi, User
              </span>
              <svg
                :class="avatarTextColor"
                class="pl-2 h-2"
                version="1.1"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 129 129"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                enable-background="new 0 0 129 129"
              >
                <g>
                  <path
                    d="m121.3,34.6c-1.6-1.6-4.2-1.6-5.8,0l-51,51.1-51.1-51.1c-1.6-1.6-4.2-1.6-5.8,0-1.6,1.6-1.6,4.2 0,5.8l53.9,53.9c0.8,0.8 1.8,1.2 2.9,1.2 1,0 2.1-0.4 2.9-1.2l53.9-53.9c1.7-1.6 1.7-4.2 0.1-5.8z"
                  />
                </g>
              </svg>
            </button>
            <div
              id="userMenu"
              :class="bgColor"
              class="rounded shadow-md mt-2 absolute mt-12 pin-t pin-r min-w-full overflow-auto z-30 invisible"
            >
              <ul class="list-reset">
                <li>
                  <a
                    href="#"
                    :class="linksColor"
                    class="px-4 py-2 block no-underline hover:no-underline"
                    >My account</a
                  >
                </li>
                <li>
                  <a
                    href="#"
                    :class="linksColor"
                    class="px-4 py-2 block no-underline hover:no-underline"
                    >Notifications</a
                  >
                </li>
                <li><hr class="border-t mx-2 border-grey-light" /></li>
                <li>
                  <a
                    href="#"
                    :class="linksColor"
                    class="px-4 py-2 block no-underline hover:no-underline"
                    >Logout</a
                  >
                </li>
              </ul>
            </div>
          </div>

          <div class="block lg:hidden pr-4">
            <button
              id="nav-toggle"
              :class="hoverColor"
              class="flex items-center px-3 py-2 border rounded text-grey border-grey-dark hover:border-teal appearance-none focus:outline-none"
            >
              <svg
                class="fill-current h-3 w-3"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <title>Menu</title>
                <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
              </svg>
            </button>
          </div>
        </div>
      </div>

      <div
        id="nav-content"
        :class="bgColor"
        class="w-full flex-grow lg:flex lg:items-center lg:w-auto hidden lg:block mt-2 lg:mt-0 z-20"
      >
        <ul class="list-reset lg:flex flex-1 items-center px-4 md:px-0">
          <li class="mr-6 my-2 md:my-0">
            <a
              href="#"
              :class="menuActiveLinkColor"
              class="block py-1 md:py-3 pl-1 align-middle no-underline border-b-2"
            >
              <i :class="menuActiveIconColor" class="fas fa-home fa-fw mr-3"></i
              ><span class="pb-1 md:pb-0 text-sm">Home</span>
            </a>
          </li>
          <li class="mr-6 my-2 md:my-0">
            <a
              href="#"
              :class="[
                menuLinksColor,
                darkMode ? 'hover:border-pink-light' : 'hover:border-pink'
              ]"
              class="block py-1 md:py-3 pl-1 align-middle text-grey no-underline border-b-2"
            >
              <i class="fas fa-tasks fa-fw mr-3"></i
              ><span class="pb-1 md:pb-0 text-sm">Tasks</span>
            </a>
          </li>
          <li class="mr-6 my-2 md:my-0">
            <a
              href="#"
              :class="[
                menuLinksColor,
                darkMode ? 'hover:border-purple-light' : 'hover:border-purple'
              ]"
              class="block py-1 md:py-3 pl-1 align-middle text-grey no-underline border-b-2"
            >
              <i class="fa fa-envelope fa-fw mr-3"></i
              ><span class="pb-1 md:pb-0 text-sm">Messages</span>
            </a>
          </li>
          <li class="mr-6 my-2 md:my-0">
            <a
              href="#"
              :class="[
                menuLinksColor,
                darkMode ? 'hover:border-green-light' : 'hover:border-green'
              ]"
              class="block py-1 md:py-3 pl-1 align-middle text-grey no-underline border-b-2"
            >
              <i class="fas fa-chart-area fa-fw mr-3"></i
              ><span class="pb-1 md:pb-0 text-sm">Analytics</span>
            </a>
          </li>
          <li class="mr-6 my-2 md:my-0">
            <a
              href="#"
              :class="[
                menuLinksColor,
                darkMode ? 'hover:border-red-light' : 'hover:border-red'
              ]"
              class="block py-1 md:py-3 pl-1 align-middle text-grey no-underline border-b-2"
            >
              <i class="fa fa-wallet fa-fw mr-3"></i
              ><span class="pb-1 md:pb-0 text-sm">Payments</span>
            </a>
          </li>
        </ul>

        <div class="relative pull-right pl-4 pr-4 md:pr-0">
          <input
            type="search"
            placeholder="Search"
            :class="searchColor"
            class="w-full text-sm transition border rounded py-1 px-2 pl-10 appearance-none leading-normal"
          />
          <div
            class="absolute sea,rch-icon"
            style="top: 0.375rem;left: 1.75rem;"
          >
            <svg
              :class="searchIconColor"
              class="fill-current pointer-events-none w-4 h-4"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
            >
              <path
                d="M12.9 14.32a8 8 0 1 1 1.41-1.41l5.35 5.33-1.42 1.42-5.33-5.34zM8 14A6 6 0 1 0 8 2a6 6 0 0 0 0 12z"
              ></path>
            </svg>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  computed: {
    darkMode() {
      return this.$store.state.darkMode;
    },
    bgColor() {
      return this.darkMode ? 'bg-black' : 'bg-white';
    },
    textColor() {
      return this.darkMode ? 'text-grey-lightest' : 'text-black';
    },
    textColorAlt() {
      return this.darkMode ? 'text-grey-lightest' : '';
    },
    linksColor() {
      return this.darkMode
        ? 'text-grey-lightest hover:bg-grey-darkest'
        : 'text-black hover:bg-grey-light';
    },
    hoverColor() {
      return this.darkMode ? 'hover:text-grey-lightest' : 'hover:text-black';
    },
    iconColor() {
      return this.darkMode
        ? `text-blue-light ${this.icon}`
        : `text-orange-dark  ${this.icon}`;
    },
    icon() {
      return this.darkMode ? 'fa-moon' : 'fa-sun';
    },
    avatarTextColor() {
      return this.darkMode ? 'fill-current text-grey-lightest' : '';
    },
    searchColor() {
      return this.darkMode
        ? 'bg-black text-grey-light border-grey-darkest focus:outline-none focus:border-grey-dark'
        : 'bg-grey-lightest text-grey-darkest focus:outline-none focus:border-grey-darker';
    },
    searchIconColor() {
      return this.darkMode ? 'text-grey' : 'text-grey-darkest';
    },
    menuActiveLinkColor() {
      return this.darkMode
        ? 'text-blue-light hover:text-grey-lightest border-blue-light hover:border-blue-light'
        : 'text-orange-dark hover:text-black border-orange-dark hover:border-orange-dark';
    },
    menuActiveIconColor() {
      return this.darkMode ? 'text-blue-light' : 'text-orange-dark';
    },
    menuLinksColor() {
      return this.darkMode
        ? 'hover:text-grey-lightest border-black'
        : 'hover:text-black border-white';
    }
  },
  mounted() {
    const userMenuDiv = document.getElementById('userMenu');
    const userMenu = document.getElementById('userButton');

    const navMenuDiv = document.getElementById('nav-content');
    const navMenu = document.getElementById('nav-toggle');

    document.onclick = check;

    function check(e) {
      const target = (e && e.target) || (event && event.srcElement);

      // User Menu
      if (!checkParent(target, userMenuDiv)) {
        // click NOT on the menu
        if (checkParent(target, userMenu)) {
          // click on the link
          if (userMenuDiv.classList.contains('invisible')) {
            userMenuDiv.classList.remove('invisible');
          } else {
            userMenuDiv.classList.add('invisible');
          }
        } else {
          // click both outside link and outside menu, hide menu
          userMenuDiv.classList.add('invisible');
        }
      }

      // Nav Menu
      if (!checkParent(target, navMenuDiv)) {
        // click NOT on the menu
        if (checkParent(target, navMenu)) {
          // click on the link
          if (navMenuDiv.classList.contains('hidden')) {
            navMenuDiv.classList.remove('hidden');
          } else {
            navMenuDiv.classList.add('hidden');
          }
        } else {
          // click both outside link and outside menu, hide menu
          navMenuDiv.classList.add('hidden');
        }
      }
    }

    function checkParent(t, elm) {
      while (t.parentNode) {
        if (t === elm) {
          return true;
        }
        t = t.parentNode;
      }
      return false;
    }
  }
};
</script>
