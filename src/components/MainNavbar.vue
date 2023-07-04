<template>
  <div>
    <div class="center">
      <router-link :to="{ name: 'Home' }"
            >
            <img src="@/assets/logo1.png" class="logo"/> 
        </router-link>
    </div>
    <!-- <nav
      class="navbar is-fixed-top"
      role="navigation"
      aria-label="main navigation"
      style="height: 70px; background-color: rgb(255, 255, 255, 0.4)"
    >
      <div class="navbar-brand" style="margin-left: 5px">
        <router-link :to="{ name: 'Home' }"
          >
          <img src="@/assets/logo1.png" class="logo"/> 
      </router-link>

        <a
          role="button"
          class="navbar-burger"
          aria-label="menu"
          aria-expanded="false"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>

      <div id="navbarBasicExample" class="navbar-menu has-text-left key">
        <div class="navbar-start is-hidden-tablet"></div>

        <div class="navbar-end" style="margin-right: 5px">
          <div class="navbar-item">
            <router-link :to="{ name: 'About' }" class="nav-link pad"
              >About Us</router-link
            >
          </div>
          <div class="navbar-item">
            <router-link :to="{ name: 'Home' }" class="nav-link pad"
              >How it Works</router-link
            >
          </div>
          <div class="navbar-item">
            <router-link :to="{ name: 'Home' }" class="nav-link pad"
              >FAQs</router-link
            >
          </div>
          <div class="navbar-item">
            <template>
            
              <template v-if="!$store.state.auth.isLoggedIn">
              <router-link :to="{ name: 'Home' }" class="button fmt-button"
                >Log in</router-link
              >
            </template>
            <template>
            <template v-else> 
              <router-link
                :to="{ name: 'Home' }"
                class="button fmt-button-1"
                >Dashboard</router-link
              >
            </template>
          </div>
          <div class="navbar-item">
            <template>
            <template v-if="!$store.state.auth.isLoggedIn"> 
              <router-link :to="{ name: 'Home' }" class="button fmt-button-2"
                >Get Started</router-link
              >
            </template>
            <template>
            <template v-else> 
              <div
                style="cursor: pointer"
                @click="logOut"
                class="button fmt-button-3"
              >
                Log out
              </div>
            </template>
          </div>
        </div>
      </div>
    </nav> -->
  </div>
</template>

<script>
// import { mapActions } from "vuex";


export default {
  name: "MainNavbar",
  data() {
    return {};
  },
  mounted() {
    // mobile menu
    // const burgerIcon = document.querySelector(".navbar-burger");
    // const navbarMenu = document.querySelector("#navbarBasicExample");

    // burgerIcon.addEventListener("click", () => {
    //   navbarMenu.classList.toggle("is-active");
    // });
  },
  methods: {
    // ...mapActions({
    //   logOutUser: "auth/logOutUser",
    // }),
    async logOut() {
      // console.log('logout pinged')
      try {
        await this.logOutUser();
        this.$router.push({ name: "Login" });
      } catch (error) {
        return error;
      }
    },
  },
};
</script>

<style scoped>
/* @import "../../node_modules/bulma/"; */
@import "~bulma/css/bulma.css";


@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500&display=swap");
* {
  margin: 0 -5px;
  padding: 0;
  padding-left: 7px;
  padding-right: 7px;
  box-sizing: border-box;
  font-family: "Quicksand", sans-serif;
}
.nav-link {
  text-decoration: none;
  color: #001951;
  font-family: "Quicksand" sans-serif;
  font-size: 16px;
  font-weight: 600;
  font-style: normal;
  cursor: pointer;
}
.fmt-button {
  background: #fff;
  border-radius: 5px;
  border: 1px solid #001951;
  color: #001951;
  padding: 10px 40px;
  text-align: center;
  cursor: pointer;
}
.fmt-button-1 {
  background: #001951;
  border-radius: 5px;
  border: 1px solid #001951;
  color: #fff;
  padding: 10px 40px;
  text-align: center;
  cursor: pointer;
}
.fmt-button-2 {
  background: #ffc100;
  border-radius: 5px;
  border: 1px solid #ffc100;
  color: #001951;
  padding: 10px 40px;
  text-align: center;
  cursor: pointer;
  margin-left: 10px;
}
.fmt-button-3 {
  background: #ff0202;
  border-radius: 5px;
  border: 1px solid #ff0202;
  color: #fdfdff;
  padding: 10px 40px;
  text-align: center;
  cursor: pointer;
  margin-left: 10px;
}

.pad {
  padding: 10px 20px;
}

.logo {
  max-width: 180px;
  margin-top: 10px;
}

@media only screen and (max-width: 800px) {
  * {
    margin: 0 -5px;
  }

  .fmt-button,
  .fmt-button-1 {
    margin-left: 7px;
  }
  .fmt-button,
  .fmt-button-1,
  .fmt-button-2,
  .fmt-button-3 {
    width: 150px;
  }
  .key {
    padding-left: 15px;
    padding-top: 20px;
  }
  .logo {
    max-width: 150px;
    margin-top: 15px;
  }
}
</style>
