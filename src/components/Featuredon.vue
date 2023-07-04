<template>
  <div>
    <div class="element-featured">
      <h3>Featured on</h3>
    </div>
    <div class="container">
      <img src="@/assets/bella.png" alt="" />
      <img src="@/assets/irokotv.png" alt="" />
      <img src="@/assets/guardian.png" alt="" />
      <img style="max-height: 80px" src="@/assets/businessday.png" alt="" />
      <img src="@/assets/techcaba.png" alt="" />
    </div>
  </div>
</template>

<script>
export default {
};
</script>

<style scoped>
@import "~bulma/css/bulma.css";

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Quicksand", sans-serif;
}

.element-featured {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin: 1.5em;
  padding: 1em;
}
.element-featured > h3 {
  margin-bottom: 1rem;
  font-weight: 500;
  font-size: 16px;
  line-height: 141.19%;
  letter-spacing: 0.02em;
  color: #808080;
}
.container {
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}
.container > img {
  filter: grayscale(100%);
  margin: 1em 1em;
  max-width: 185px;
  max-height: 30px;
  justify-content: space-between;
  margin: auto;
}
@media only screen and (max-width: 800px) {
  .container {
    flex-direction: column;
    width: 100%;
    padding-left: 0;
    margin: auto;
  }
  .container > img {
    margin-top: 25px;
  }
  .container > img:nth-child(1) {
    margin-top: -20px;
    max-width: 200px;
  }
}
</style>
