<template>
  <footer>
    <div class="footer-container">
      <div class="row">
        <div class="left-col">
          <img src="@/assets/logo1.png" class="logo" />
          <!-- <div class="btn-container">
            <div class="btn">
              <i class="bx bxl-play-store"></i>
              <div class="group">
                <div class="format">Download on</div>
                <div class="format-2">Google Play</div>
              </div>
            </div>
            <div class="btn">
              <i class="bx bxl-apple"></i>
              <div class="group">
                <div class="format">Get it on</div>
                <div class="format-2">Apple Store</div>
              </div>
            </div>
          </div> -->
          <div class="social-media">
            <a class="bx-fw bx bxl-facebook facebook" href="https://web.facebook.com/Propfunds-103118648774491"
              target="_blank" rel="noopener noreferrer"></a>
            <a class="bx-fw bx bxl-twitter twitter" href="https://twitter.com/Propfundsng?s=08" target="_blank"
              rel="noopener noreferrer"></a>
            <a class="bx-fw bx bxl-instagram instagram" href="https://www.instagram.com/propfunds_ng/" target="_blank"
              rel="noopener noreferrer"></a>
            <a class="bx-fw bx bxl-linkedin linkedin"
              href="https://www.linkedin.com/company/propfundsng/about/?viewAsMember=true" target="_blank"
              rel="noopener noreferrer"></a>
          </div>
        </div>
        <div class="items">
          <div class="col">
            <h4>Links</h4>
            <ul>
              <li>
                <router-link :to="{ name: 'About' }" class="nav-link">
                  About</router-link>
              </li>
              <li>
                <router-link :to="{ name: 'Home' }" class="nav-link">
                  How it Works</router-link>
              </li>
              <li>
                <router-link :to="{ name: 'Home' }" class="nav-link">
                  FAQs
                </router-link>
              </li>
              <li>
                <router-link :to="{ name: 'Home' }" class="nav-link">
                  Get Started
                </router-link>
              </li>
            </ul>
          </div>
          <div class="col">
            <h4>Company</h4>
            <ul>
              <li>
                <router-link :to="{ name: 'Home' }" class="nav-link">
                  Terms & Conditions</router-link>
              </li>
              <li>
                <router-link :to="{ name: '' }" class="nav-link">
                  Privacy Policy</router-link>
              </li>
            </ul>
          </div>
          <div class="col ccl">
            <h4>Get in touch</h4>
            <ul>
              <li>+234 818 100 8962</li>
              <li>
                Odusami Street, Off Wemco Street Ogba, Ikeja,<br />
                Lagos.
              </li>
              <li>info@propfunds.ng</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
@import "~bulma/css/bulma.css";

@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500&display=swap");

/* * {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Quicksand" sans-serif;
} */
.row {
  display: flex;
  margin-left: 15px;
  margin-right: 20px;
}
.social-media > a {
  text-align: center;
  text-decoration: none;
  
}

.social-media{
margin-top: 13px;
}
.facebook {
  background: #ffe6e2;
  height: 40px;
  width: 40px;
  margin-right: 10px;
  text-align: center;
  color: #fc573b;
  padding: 10px 0;
  border-radius: 8px;
  cursor: pointer;
}
.twitter {
  background: #f5e6fe;
  height: 40px;
  width: 40px;
  margin-right: 10px;
  text-align: center;
  color: #be63f9;
  padding: 10px 0;
  border-radius: 8px;
  cursor: pointer;
}
.instagram {
  background: #ffe6e2;
  height: 40px;
  width: 40px;
  margin-right: 10px;
  text-align: center;
  color: #fc573b;
  padding: 10px 0;
  border-radius: 8px;
  cursor: pointer;
}
.linkedin {
  background: #f5e6fe;
  height: 40px;
  width: 40px;
  margin-right: 10px;
  text-align: center;
  color: #be63f9;
  padding: 10px 0;
  border-radius: 8px;
  cursor: pointer;
}
.left-col {
  text-align: left;
  margin-right: 24px;
}
.logo {
  cursor: pointer;
  max-width: 180px;
}
.btn-container {
  width: 100%;
  display: flex;
}
.btn-container > .btn {
  display: flex;
  margin: 7% 0;
  background-color: #001951;
  border: none;
  border-radius: 5px;
  color: white;
  font-family: "Quicksand", sans-serif;
  font-size: 14px;
  cursor: pointer;
  width: 150px;
  align-items: center;
  justify-content: center;
  padding: 8px 0;
  margin-right: 20px;
}

.btn-container > .btn > i {
  font-size: 18px;
}
.group {
  margin-left: 20px;
}
.group > .format {
  font-weight: 500;
  font-size: 7px;
  line-height: 12px;
}

.group > .format-2 {
  font-weight: 400;
  font-size: 14px;
}

.col > h4 {
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  color: #000;
  margin-bottom: 20px;
  text-align: left;
}
.nav-link {
  text-decoration: none;
}
ul {
  list-style: none;
}
.col {
  width: 200px;
  margin: 0 15px;
  margin-left: 35px;
}
.col ul li {
  font-style: normal;
  font-size: 14px;
  font-weight: 400;
  color: #777;
  align-content: center;
  justify-content: left;
  padding-bottom: 15px;
  text-align: left;
}
.nav-link {
  color: #777;
}
.items {
  display: flex;
  padding-left: 90px;
}
@media only screen and (max-width: 800px) {
  .row {
    flex-direction: column;
    justify-content: center;
  }
  .col {
    margin: 0;
    margin-top: 10px;
    margin-right: 5.2rem;
  }
  .col ul li {
    padding-left: 0;
  }
  .col > h4 {
    text-align: left;
  }
  .items {
    display: flex;
    justify-content: flex-start;
    flex-basis: 50%;
    flex-wrap: wrap;
    padding-left: 0px;
    margin-top: 30px;
  }
  .col {
    width: 100px;
    margin: 0 35px;
    margin-top: 20px;
    margin-left: 15px;
  }
  .ccl{
    width: 150px;
  }
}
</style>
