<!-- <template>
  <nav class="navbar navbar-expand-lg">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">
        <img src="../assets/images/iFlowspace-Logo.png" alt="" />
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon custom-toggler"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link" href="#">about</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">what we do</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">residential</a>
          </li>
          <li class="nav-item">
            <a class="nav-link">commercial</a>
          </li>
          <li class="nav-item">
            <a class="nav-link">calculator</a>
          </li>
          <li class="nav-item last-item">
            <a class="nav-itam-button">request a quote</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {},
};
</script>

<style>
.navbar {
  padding: 0 40px;
  background-color: #0e2442;
}

.navbar-nav {
  margin-left: auto;
  width: 95%;
  display: flex;
  justify-content: space-between;
}

.navbar-nav .nav-link {
  text-transform: uppercase;
  font-size: 16px;
  color: #fff;
  border-bottom: 1px solid transparent;
}

.navbar-nav .nav-link:hover {
  color: #eac7a7;
  border-bottom: 1px solid #eac7a7;
}

.last-item {
  width: 200px;
}

.nav-itam-button {
  display: inline-block;
  width: 100%;
  height: 100%;
  padding: 8px 10px;
  text-align: center;
  text-decoration: none;
  text-transform: uppercase;
  font-size: 16px;
  color: #fff;
  background-color: #e57661;
  border-radius: 5px;
  cursor: pointer;
}

@media (max-width: 991px) {
  .navbar {
    padding: 10px 10px 30px 10px;
  }

  .navbar-nav {
    margin-left: 0;
    padding-left: 20px;
    width: 100%;
    row-gap: 10px;
  }

  .navbar-toggler {
    border-color: #fff !important;
  }
  .navbar-toggler:focus {
    text-decoration: none;
    outline: 0;
    box-shadow: none;
}
  .navbar-toggler-icon.custom-toggler {
    background-image: url("data:image/svg+xml;charset=UTF8,%3csvg viewBox='0 0 30 30' xmlns='http://www.w3.org/2000/svg'%3e%3cpath stroke='rgba(255,255,255,1)' stroke-width='2' d='M4 7h22M4 15h22M4 23h22'/%3e%3c/svg%3e");
  }
}
</style> -->
<template>
  <div>
    <nav class="bg-[#0e2442] px-4 py-2 md:px-40">
      <div class=" mx-auto flex items-center justify-between flex-wrap">
        <a class="flex-shrink-0" href="#">
          <img class=" w-28 " src="../assets/images/iFlowspace-Logo.png" alt="iFlowspace Logo" />
        </a>
        <div class="block lg:hidden">
          <button
            class="flex items-center px-3 py-2 border rounded text-white border-white"
            @click="toggleSidebar"
          >
            <svg
              class="fill-current h-3 w-3"
              viewBox="0 0 30 30"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                stroke="rgba(255,255,255,1)"
                stroke-width="2"
                d="M4 7h22M4 15h22M4 23h22"
              />
            </svg>
          </button>
        </div>
        <div class="hidden lg:flex lg:items-center lg:w-[85%]">
          <ul class="text-white lg:items-center lg:flex-grow lg:flex lg:justify-between space-y-4 lg:space-y-0 lg:space-x-4 w-full lg:w-auto">
            <li>
              <a class="block lg:inline-block uppercase text-lg hover:text-[#eac7a7] border-b-2 border-transparent hover:border-[#eac7a7]" href="#">about</a>
            </li>
            <li>
              <a class="block lg:inline-block uppercase text-lg hover:text-[#eac7a7] border-b-2 border-transparent hover:border-[#eac7a7]" href="#">what we do</a>
            </li>
            <li>
              <a class="block lg:inline-block uppercase text-lg hover:text-[#eac7a7] border-b-2 border-transparent hover:border-[#eac7a7]" href="#">residential</a>
            </li>
            <li>
              <a class="block lg:inline-block uppercase text-lg hover:text-[#eac7a7] border-b-2 border-transparent hover:border-[#eac7a7]">commercial</a>
            </li>
            <li>
              <a class="block lg:inline-block uppercase text-lg hover:text-[#eac7a7] border-b-2 border-transparent hover:border-[#eac7a7]">calculator</a>
            </li>
            <li class="w-[330px] lg:w-auto">
              <a class="block w-full text-center uppercase text-lg text-white bg-[#e57661] rounded py-2 px-4 cursor-pointer hover:bg-[#d96551]" href="#">request a quote</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- Overlay -->
    <div :class="overlayClasses" class="fixed inset-0 bg-gray-700 z-40 lg:hidden transition duration-150 delay-150"></div>

    <!-- Sidebar -->
    <div :class="sidebarClasses" class="fixed inset-y-0 left-0 bg-[#0e2442] w-9/12 z-50 transition-transform duration-200 delay-200 transform lg:hidden">
      <div class="container mx-auto py-2 px-4">
        <div class="flex justify-between ">
          <img class="w-28" src="../assets/images/iFlowspace-Logo.png" alt="iFlowspace Logo" />
          <button @click="toggleSidebar" class="text-white">
            <svg
              class="fill-current h-6 w-6"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                d="M6.707 5.293a1 1 0 00-1.414 1.414L10.586 12l-5.293 5.293a1 1 0 001.414 1.414L12 13.414l5.293 5.293a1 1 0 001.414-1.414L13.414 12l5.293-5.293a1 1 0 00-1.414-1.414L12 10.586 6.707 5.293z"
              />
            </svg>
          </button>
        </div>
        <ul class="text-white mt-8 space-y-4 px-4">
          <li>
            <a class="block uppercase text-lg hover:text-[#eac7a7] border-b-2 border-transparent hover:border-[#eac7a7]" href="#">about</a>
          </li>
          <li>
            <a class="block uppercase text-lg hover:text-[#eac7a7] border-b-2 border-transparent hover:border-[#eac7a7]" href="#">what we do</a>
          </li>
          <li>
            <a class="block uppercase text-lg hover:text-[#eac7a7] border-b-2 border-transparent hover:border-[#eac7a7]" href="#">residential</a>
          </li>
          <li>
            <a class="block uppercase text-lg hover:text-[#eac7a7] border-b-2 border-transparent hover:border-[#eac7a7]">commercial</a>
          </li>
          <li>
            <a class="block uppercase text-lg hover:text-[#eac7a7] border-b-2 border-transparent hover:border-[#eac7a7]">calculator</a>
          </li>
          <li>
            <a class="block absolute left-10 right-10 bottom-10 uppercase text-lg text-white bg-[#e57661] rounded py-2 px-4 text-center cursor-pointer hover:bg-[#d96551]" href="#">request a quote</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isSidebarOpen: false,
    };
  },
  computed: {
    sidebarClasses() {
      return {
        'translate-x-0': this.isSidebarOpen,
        '-translate-x-full': !this.isSidebarOpen,
      };
    },
    overlayClasses() {
      return {
        'opacity-80': this.isSidebarOpen,
        'opacity-0': !this.isSidebarOpen,
        'block': this.isSidebarOpen,
        'hidden': !this.isSidebarOpen
      };
    },
  },
  methods: {
    toggleSidebar() {
      this.isSidebarOpen = !this.isSidebarOpen;
    },
  },
};
</script>

<style scoped>

</style>
