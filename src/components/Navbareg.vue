<template>
    <header class="header">
        <nav class="navbar">
        <router-link :to="{ name: 'Home'}" class="nav-logo"><img src="@/assets/logo1.png" /></router-link>
        <ul class="nav-menu">
            <li class="nav-item">
            <router-link :to="{ name: 'Home'}" class="nav-link fmt-button">Sign in</router-link>
            </li>
            <li class="nav-item">
            <router-link :to="{ name: 'Home'}" class="nav-link fmt-button-2">Register</router-link>
            </li>
        </ul>
        <div class="hamburger" @click="mobileMenu()">
            <span class="bar"></span>
            <span class="bar"></span>
            <span class="bar"></span>
        </div>
        </nav>
    </header>
</template>

<script>
export default {
    data() {
        return {
        }
    },
    methods: {

    mobileMenu() {
    const hamburger = document.querySelector(".hamburger");
        const navMenu = document.querySelector(".nav-menu");
        
        hamburger.classList.toggle("active");
        navMenu.classList.toggle("active");
    },
    closeMenu() {
        const hamburger = document.querySelector(".hamburger");
        const navMenu = document.querySelector(".nav-menu");

        hamburger.classList.remove("active");
        navMenu.classList.remove("active");
    }

    },
}
</script>

<style scoped>
@import "~bulma/css/bulma.css";

@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500&display=swap");


* {
  margin: 0 5px;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Quicksand', sans-serif;
}



.nav-logo img {
    max-width: 150px;
  }

.nav-menu > li {
  list-style-type: none;
}

.nav-link {
  text-decoration: none;
  color: #001951;
  font-family: 'Quicksand' sans-serif;
  font-size: 16px;
  font-weight: 600;
  font-style: normal;
}
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 0;
}

.hamburger {
  display: none;
}
.bar {
  display: block;
  width: 25px;
  height: 3px;
  margin: 5px auto;
  animation: all 0.3s ease-in-out;
  transition: all 0.3s ease-in-out;
  background-color: #101010;
}
.nav-menu {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-item {
  margin-left: 1rem;
}
.fmt-button {
    background: #fff;
    border-radius: 5px;
    border: 1px solid #001951;
    color: #001951;
    padding: 10px 40px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 0;
    cursor: pointer;
}
.fmt-button-2 {
    background: #FFC100;
    border-radius: 5px;
    border: 1px solid #FFC100;
    color: #001951;
    padding: 10px 40px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 0;
    cursor: pointer;
}
.btn{
    background: #001951;
    border-radius: 5px;
    border: none;
    color: white;
    padding: 10px 40px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    transition: opacity .3s linear;
}

@media only screen and (max-width:800px) {
    *{margin: 0;}
    
    .nav-menu {
      position: fixed;
      left: -100%;
      top: 4rem;
      flex-direction: column;
      background-color: #fff;
      width: 100%;
      border-radius: 10px;
      text-align: center;
      transition: 0.3s;
      box-shadow: 0 10px 27px rgba(0, 0, 0, 0.05);
    }
    .nav-menu.active {
      left: 0;
    }
  
    .nav-item {
      margin: 2.5rem 0;
      margin-right: 10.2rem;
      font-size: 16px;
      font-weight: 500;
    }
    .hamburger {
      display: block;
      cursor: pointer;
    }
    .hamburger.active .bar:nth-child(2) {
      opacity: 0;
    }
  
    .hamburger.active .bar:nth-child(1) {
      transform: translateY(8px) rotate(45deg);
    }
  
    .hamburger.active .bar:nth-child(3) {
      transform: translateY(-8px) rotate(-45deg);
    }
  
    .nav-logo img {
      max-width: 126.13px;
    }

}
</style>