<template>
  <div class="banner-section">
    <div class="banner-container">
      <div class="item">
        <h1 class="head">$327B</h1>
        <p>Quarterly volume traded</p>
      </div>
      <div class="item">
        <h1 class="head">100+</h1>
        <p>Countries supported</p>
      </div>
      <div class="item">
        <h1 class="head">73+M</h1>
        <p>Verified users</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Banner",
};
</script>

<style scoped>
.banner-section {
  background-color: rgb(0, 82, 255);
  height: 495px;
}
.banner-container {
  width: 70%;
  margin: 0 auto;
  display: flex;
  align-items: center;
  flex-direction: column;
  height: 200px;
}
.item {
  margin-top: 45px;
}
.head {
  font-size: 56px;
  text-align: center;
  color: white;
}
p {
  text-align: center;
  line-height: 24px;
  font-size: 16px;
  opacity: 0.7;
  color: white;
}
@media only screen and (min-width: 992px) {
  .banner-section {
    background-color: rgb(0, 82, 255);
    height: 200px;
  }
  .banner-container {
    justify-content: space-between;
    align-items: center;
    flex-direction: row;
    height: 200px;
  }
  .item {
    width: 25%;
    margin-top: 0;
  }
}
</style>