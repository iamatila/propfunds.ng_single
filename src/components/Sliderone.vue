<template>
  <div>
    <div class="container desktopView">
      <div class="cover">
        <div class="row">
          <div class="col-2">
            <div class="group">
              <div class="row-1">
                <h2>
                  WHY REAL ESTATE IS A<br />
                  SUPERIOR INVESTMENT
                </h2>
              </div>
              <div class="row-1">
                <p style="line-height: 200%">
                  On its own, real estate investment offers cash flow, tax
                  breaks, equity building, competitive risk adjusted returns,
                  and serves as a security against inflation. When you invest in
                  real estate, you enjoy; predictable cash flows, increase in
                  value appreciation, revenue through rental income, tax
                  advantages, diversification and build massive wealth.
                </p>
              </div>
              <div class="row-1">
                <div class="dis" style="display: flex">
                  <router-link :to="{ name: 'Home' }" class="fmt-button-2"
                    >Get started</router-link
                  >
                </div>
              </div>
            </div>
          </div>
          <div class="col-2">
            <img src="@/assets/s3-img.png" alt="" />
          </div>
        </div>
      </div>
    </div>
    <div class="container-flex mobileView">
      <h3 style="color: #000000">WHY REAL ESTATE IS A SUPERIOR INVESTMENT</h3>
      <p style="line-height: 200%">
        On its own, real estate investment offers cash flow, tax breaks, equity
        building, competitive risk adjusted returns, and serves as a security
        against inflation. When you invest in real estate, you enjoy;
        predictable cash flows, increase in value appreciation, revenue through
        rental income, tax advantages, diversification and build massive wealth.
      </p>
      <router-link :to="{ name: 'Home' }" class="fmt-button-2"
        >Get started</router-link
      >
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

.container {
  display: flex;
  align-content: center;
}
.cover {
  width: 100%;
  height: 400px;
  border-radius: 30px;
  margin-top: 10px;
}
.row {
  padding-bottom: 40px;
  display: flex;
  flex-direction: row-reverse;
  align-items: center;
  justify-content: space-around;
}
.col-2 {
  flex-basis: 50%;
  min-width: 300px;
  overflow: hidden;
}
.col-2 h1 {
  font-family: "Quicksand", sans-serif;
  font-style: normal;
  font-weight: bold;
  font-size: 40px;
  line-height: 118.19%;
  color: #000000;
  text-align: left;
}
.col-2 > img {
  max-width: 546px;
  width: 100%;
  height: 422px;
  border-radius: 25px;
  overflow: hidden;
}
.fmt-button {
  background: #fff;
  border-radius: 5px;
  border: 1px solid #fff;
  color: #001951;
  padding: 10px 10px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 18px;
  margin: 4px 3px;
  cursor: pointer;
  width: fit-content;
}
.fmt-button-2 {
  background: #001951;
  border-radius: 5px;
  border: 1px solid #001951;
  color: #fff;
  padding: 10px 40px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  margin-right: 5px;
  cursor: pointer;
}
.row-1 {
  justify-content: left;
  margin: 30px 0 10px 50px;
  width: 100%;
  flex-basis: 50%;
}
.row-1 > h1 {
  font-size: 30px;
}
.row-1 > p {
  text-align: left;
  width: 424px;
}
.dis > a > span > img {
  padding-right: 2px;
  width: 16px;
}
.group {
  margin-top: 80px;
}
.mobileView {
  display: none;
}
a {
  cursor: pointer;
}
.dis {
  cursor: pointer;
}
@media only screen and (max-width: 800px) {
  .desktopView {
    display: none;
  }
  .container-flex {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1em 1em;
    margin-top: 56px;
  }
  .container-flex p {
    font-family: "Quicksand", sans-serif;
    font-weight: normal;
    font-size: 1rem;
    line-height: 20px;
    text-align: center;
    color: #484848;
    margin: 20px 0;
  }
  .container-flex h3 {
    font-family: "Quicksand", sans-serif;
    font-weight: bold;
    font-size: 24px;
    line-height: 32px;
    text-align: center;
    letter-spacing: 0.02em;
    color: #5d5fef;
  }
  .container-flex a {
    cursor: pointer;
    text-decoration: none;
  }
  .buttonMob {
    background: #001951;
    border-radius: 5px;
    border: none;
    color: white;
    padding: 14px 59.3px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
  }
}
</style>
