<template>
  <div>
    <div class="svg-cover">
      <svg
        width="1440"
        height="835"
        viewBox="0 0 1440 835"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M1231.4 0.505093L1439.5 99.5033V726.309L989.946 797.502L386.054 834.496L0.5 726.357V55.7531L1231.4 0.505093Z"
          fill="#EFF7FF"
          fill-opacity="0.65"
          stroke="#fff"
        />
        <path
          d="M1439.5 180.372V822.432L755.063 734.812L755.003 734.804L754.942 734.811L0.5 822.439V17.5598L1439.5 180.372Z"
          fill="#DDF5FF"
          fill-opacity="0.33"
          stroke="#fff"
        />
      </svg>
    </div>
    <div class="cover-1 desktopView">
      <div class="element-featured">
        <h3></h3>
      </div>
      <div class="container">
        <div class="row">
          <div class="col">
            <h2>A DIFFERENT KIND OF REAL ESTATE INVESTMENT EXPERIENCE</h2>
            <ul>
              <li style="line-height: 200%">
                Propfunds provides a real estate investment experience like no
                other, by the provision of a; platform where you can buy and
                sell your properties, co-own several actual properties with
                other investors, monitor your property, and best of all; buy
                properties, or own a slot seamlessly.
              </li>
            </ul>
          </div>
          <div class="col">
            <img src="@/assets/slider-two-img.png" alt="" />
          </div>
        </div>
      </div>
    </div>
    <div
      class="container-1 bg-container mobileView"
      style="flex-direction: column"
    >
      <h3 style="margin-bottom: 10px">
        A DIFFERENT KIND OF REAL ESTATE INVESTMENT EXPERIENCE
      </h3>
      <span style="line-height: 200%">
        Propfunds provides a real estate investment experience like no other, by
        the provision of a; platform where you can buy and sell your properties,
        co-own several actual properties with other investors, monitor your
        property, and best of all; buy properties, or own a slot seamlessly.
      </span>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
@import "~bulma/css/bulma.css";

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Quicksand", sans-serif;
}
.mobileView {
  display: none;
}
.cover-1 {
  position: relative;
  width: 100%;
  height: 692px;
  margin-top: 100px;
  z-index: 5;
  background-image: url("~@/assets/svg.png");
  background-size: cover;
  background-repeat: no-repeat;
  padding-top: 60px;
}
.element-featured > h3 {
  margin-bottom: 1rem;
  font-weight: 500;
  font-size: 16px;
  line-height: 141.19%;
  letter-spacing: 0.02em;
  color: #808080;
  padding-top: 20px;
}
.container {
  display: flex;
  justify-content: center;
  align-self: center;
}
.row {
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.col {
  flex-basis: 50%;
  margin-right: 25px;
}
.col > img {
  max-width: 382px;
  width: 100%;
  border-radius: 8px;
  padding-left: 20px;
}
.col > ul {
  list-style-type: none;
}
.col > ul > li {
  text-align: left;
}
.col > h1 {
  text-align: left;
  padding-bottom: 12px;

  font-size: 32px;
  line-height: 56px;
  letter-spacing: 0.02em;
}
.col > h1,
.col ul {
  width: 465px;
}
svg {
  max-width: 1440px;
  width: 100%;
  position: absolute;
  left: 0;
  margin-top: -27px;
  z-index: 1;

  display: none;
}

@media only screen and (max-width: 800px) {
  .desktopView {
    display: none;
  }
  .mobileView {
    display: block;
  }
  .container-1 {
    width: 100%;
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 1em;
  }
  .bg-container {
    background-image: url("~@/assets/svg.png");
    background-size: cover;
    background-repeat: no-repeat;

    width: 100%;
    padding: 2rem 1rem;
  }
  .bg-container > p {
    width: 16em;
    font-weight: 500;
    font-size: 16px;
    line-height: 20px;
    text-align: center;
    letter-spacing: 0.02em;
    color: #808080;
  }

  .bg-container > h3 {
    font-weight: bold;
    font-size: 24px;
    line-height: 30px;
    letter-spacing: 0.02em;
    color: #000000;
  }

  .bg-container > ul {
    padding: 0.5em 1em;
  }

  .bg-container > ul > li {
    margin-top: 0.5em;
    font-weight: 500;
    font-size: 14px;
    line-height: 22px;
    letter-spacing: 0.02em;
    color: #484848;
    text-align: left;
  }
  .bg-container > h3 {
    margin-top: 0.5em;
    font-weight: bold;
    font-size: 24px;
    line-height: 30px;
    letter-spacing: 0.02em;
    color: #000000;
  }
}
</style>
