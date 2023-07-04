<template>
  <div class="container">
  <h1 class="txt center">WE'D lOVE TO KNOW YOU</h1>
  <div>
    <div class="cover">
      <div class="box has-text-left pl-6">
        <h1 class="pt-6 is-size-3">Get in touch</h1>
        <div class="pt-4">
          <h3 class="is-size-5">Visit us</h3>
          <div class="is-size-7">
            Come say hello at our office. <br/>
            Gods Legacy Plaza <br />
            Off Acme road <br />
            Ogba, Ikeja <br />
            Lagos. <br />
          </div>
        </div>
        <div class="pt-4">
          <h3 class="is-size-5">Chat with us</h3>
          <div class="is-size-7">
            Our always friendly team is here to help <br/>
            info@propfunds.ng <br />
          </div>
        </div>
        <div class="pt-4">
          <h3 class="is-size-5">Call us on:</h3>
          <div class="is-size-7">
            Mon-Fri from 9am to 5pm <br/>
            (+234) 816-398-4131 <br />
          </div>
        </div>
        <div class="pt-4">
          <h3 class="is-size-5">Social media</h3>
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
          <!-- <p>
            Come say hello at our office. <br/>
            Gods Legacy Plaza <br />
            Off Acme road <br />
            Ogba, Ikeja <br />
            Lagos. <br />
          </p> -->
        </div>
      </div>
      <div class="pt-5">
        <form name="PropertySubscribers4/7/23" method="POST" netlify>
          <div class="row has-text-left">
            <div class="input-group">
              <p for="first_name">First Name</p>
              <input
                type="text"
                id="first_name"
                />
                <!-- placeholder="First Name" -->
                <!-- v-model="formData.first_name" -->
            </div>
            <div class="input-group">
              <p for="last_name">Last Name</p>
              <input
                type="text"
                id="last_name"
                />
                <!-- placeholder="Last Name" -->
                <!-- v-model="formData.last_name" -->
            </div>
          </div>
          <div class="row has-text-left">
            <div class="input-group">
              <p for="email">Email</p>
              <input
                type="email"
                id="email"
                />
                <!-- placeholder="Email" -->
                <!-- v-model="formData.email" -->
            </div>
            <div class="input-group">
              <p for="phone_number">Phone Number</p>
              <input
                type="number"
                id="phone_number"
                />
                <!-- placeholder="Phone Number" -->
                <!-- v-model="formData.phone_number" -->
            </div>
          </div>
          <div class="row has-text-left">
            <div class="input-group">
              <!-- <input type="text" id="country" placeholder="Country" v-model="country"> -->
              <p for="country">Country</p>
              <!-- class="select" -->
              <select
                id="country"
                name="country[]"
                multiple
                >
                <!-- v-model="formData.country" -->
                <option value="" selected disabled></option>
                <option>Nigeria</option>
                <!-- <option>Ghana</option> -->
              </select>
            </div>
            <div class="input-group">
              <!-- <input type="text" id="state" placeholder="State" v-model="state"> -->
              <p for="state">State</p>
              <select id="state" name="state[]" multiple
              >
              <!-- v-model="formData.state" -->
                <option selected disabled>--Select State--</option>
                <option value="Abia">Abia</option>
                <option value="Adamawa">Adamawa</option>
                <option value="Akwa Ibom">Akwa Ibom</option>
                <option value="Anambra">Anambra</option>
                <option value="Bauchi">Bauchi</option>
                <option value="Bayelsa">Bayelsa</option>
                <option value="Benue">Benue</option>
                <option value="Borno">Borno</option>
                <option value="Cross Rive">Cross River</option>
                <option value="Delta">Delta</option>
                <option value="Ebonyi">Ebonyi</option>
                <option value="Edo">Edo</option>
                <option value="Ekiti">Ekiti</option>
                <option value="Enugu">Enugu</option>
                <option value="FCT">Federal Capital Territory</option>
                <option value="Gombe">Gombe</option>
                <option value="Imo">Imo</option>
                <option value="Jigawa">Jigawa</option>
                <option value="Kaduna">Kaduna</option>
                <option value="Kano">Kano</option>
                <option value="Katsina">Katsina</option>
                <option value="Kebbi">Kebbi</option>
                <option value="Kogi">Kogi</option>
                <option value="Kwara">Kwara</option>
                <option value="Lagos">Lagos</option>
                <option value="Nasarawa">Nasarawa</option>
                <option value="Niger">Niger</option>
                <option value="Ogun">Ogun</option>
                <option value="Ondo">Ondo</option>
                <option value="Osun">Osun</option>
                <option value="Oyo">Oyo</option>
                <option value="Plateau">Plateau</option>
                <option value="Rivers">Rivers</option>
                <option value="Sokoto">Sokoto</option>
                <option value="Taraba">Taraba</option>
                <option value="Yobe">Yobe</option>
                <option value="Zamfara">Zamfara</option>
              </select>
            </div>
          </div>
          
            <div class="has-text-left">
              <div class="input-group">
                <p for="what_we_call_you">What would you like us to call you?</p>
                <input
                  type="text"
                  id="what_we_call_you"
                  placeholder=""
                  />
                  <!-- v-model="formData.what_we_call_you" -->
              </div>
            </div>
            <div class="has-text-left">
              <div class="input-group">
                <p for="how_you_hear_about_us">How did you hear about us?</p>
                <input
                  type="text"
                  id="how_you_hear_about_us"
                  placeholder=""
                  />
                  <!-- v-model="formData.how_you_hear_about_us" -->
              </div>
            </div>
            <div class="">
              <!-- <div class="input-group">
              <button class="button2" @click.stop="settings">
                Back
              </button>
            </div> -->
              <div class="input-group m-auto">
                <button class="button fmt-button-2 is-fullwidth" type="submit">Submit</button>
              </div>
            </div>
        </form>
      </div>
      <!-- <div class="row">
        <h2>WANT TO JOIN THE INNER CIRCLE?</h2>
        <p>
          You can now join the special group of Propfunds investors and co-earn
          several properties in no time.
        </p>
        <router-link :to="{ name: 'Home' }">
          <a href="" class="fmt-button-2">Get started</a>
        </router-link>
      </div> -->
    </div>
  </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
@import "~bulma/css/bulma.css";

/* * {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Quicksand", sans-serif;
} */

.container {
  /* display: flex; */
  align-content: center;
  margin-top: 50px;
  background-image: url("~@/assets/bg-imgslide.png");
  background-size: cover;
  background-repeat: no-repeat;
}
.cover {
  width: 100%;
  height: 700px;
  border-radius: 24px;
  margin-top: 10px;
}

.box {
  /* background-image: url("~@/assets/img-s1.png"); */
  background-color: #001951;
  color: #fff;
  width: 450px;
  height: 600px;
  border-radius: 45px;
  position: absolute;
  /* top: 2%; */
  /* left: 5%; */
  /* opacity: 0.8; */
  /* z-index: 9; */
  /* margin: 20px; */
}
.box2 {
  background-color: #fff;
  width: 450px;
  height: 500px;
  border-radius: 45px;
  position: absolute;
  left: 50%;
  margin: 20px;
}
.txt {
  font-style: normal;
  font-weight: bold;
  font-size: 32px;
  line-height: 56px;
  letter-spacing: 0.02em;
  color: #000000;
}


form {
  /* width: 100%; */
  /* max-width: 600px; */
  width: 600px;
  height: 500px;
  position: absolute;
  left: 45%;
  /* margin: 20px; */
}
.input-group {
  margin-bottom: 30px;
  position: relative;
}
input {
  width: 100%;
  padding: 10px;
  outline: 0;
  border: 2px solid grey;
  color: grey;
  font-size: 15px;
  border-radius: 8px;
}
.input-group {
  margin-bottom: 30px;
  position: relative;
}
.row {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.row > .input-group {
  flex-basis: 48%;
}

select {
  width: 100%;
  padding: 10px;
  outline: 0;
  border: 2px solid grey;
  color: grey;
  font-size: 15px;
  border-radius: 8px;
}
/* .row {
  max-width: 519px;
  justify-content: center;
  align-content: center;
  margin: auto;
  padding-top: 40px;
}
.row > h1,
p,
a {
  padding: 30px 0;
} */
/* .row > p {
  max-width: 424px;
  margin: auto;
  padding: 0 15px;
  margin-bottom: 40px;
}
.row > h1 {
  margin-top: 30px;
} */

.fmt-button-2 {
  background: #001951;
  border-radius: 5px;
  border: 1px solid #001951;
  color: #fff;
  padding: 10px 70px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  margin-right: 5px;
  cursor: pointer;
}
a {
  text-decoration: none;
}

.social-media > a {
  text-align: center;
  text-decoration: none;
  
}

.social-media{
margin-top: 13px;
}
.facebook {
  background: #fff;
  height: 40px;
  width: 40px;
  margin-right: 10px;
  text-align: center;
  color: #001951;
  padding: 10px 0;
  border-radius: 8px;
  cursor: pointer;
}
.twitter {
  background: #fff;
  height: 40px;
  width: 40px;
  margin-right: 10px;
  text-align: center;
  color: #001951;
  padding: 10px 0;
  border-radius: 8px;
  cursor: pointer;
}
.instagram {
  background: #fff;
  height: 40px;
  width: 40px;
  margin-right: 10px;
  text-align: center;
  color: #001951;
  padding: 10px 0;
  border-radius: 8px;
  cursor: pointer;
}
.linkedin {
  background: #fff;
  height: 40px;
  width: 40px;
  margin-right: 10px;
  text-align: center;
  color: #001951;
  padding: 10px 0;
  border-radius: 8px;
  cursor: pointer;
}
@media only screen and (max-width: 800px) {
  .cover {
    height: 350px;
    margin-top: 20px;
  }
  .row {
    flex-direction: column;
    justify-content: center;
  }
  .row > .input-group {
    width: 100%;
  }
  form {
    width: 100%;
    z-index: -1;
  }
}
</style>
