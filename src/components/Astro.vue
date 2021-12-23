<template>
  <div class="astro-section">
    <div class="astro-container">
      <div class="astro-text">
        <h2 class="astro-head">Earn up to $10 worth of crypto</h2>
        <p class="astro-para">
          Discover how specific cryptocurrencies work — and get a bit of each
          crypto to try out for yourself.
        </p>
        <button>Start earning</button>
      </div>
      <div class="astro-img">
        <img src="../assets/coinbanner.webp" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Astro",
};
</script>

<style scoped>
.astro-section {
  background-color: rgb(17, 51, 85);
  height: 330px;
  width: 100%;
}
.astro-container {
  display: flex;
  width: 90%;
  margin: 0 auto;
}
.astro-text {
  margin-top: 35px;
  text-align: center;
}

.astro-img {
  display: none;
}
h2 {
  line-height: 1.3;
  color: white;
  font-size: 32px;
  font-weight: 500;
  text-align: center;
}
p {
  font-size: 15px;
  line-height: 1.6;
  font-weight: 400;
  color: white;
  margin-top: 10px;
  width: 260px;
  margin: 10px auto;
}
button {
  display: block;
  font-family: inherit;
  border: 1px solid rgb(0, 82, 255);
  background-color: rgb(0, 82, 255);
  font-weight: 900;
  line-height: 14px;
  width: 140px;
  height: 50px;
  border-radius: 4px;
  color: white;
  margin: 20px auto 0;
  font-size: 18px;
}

@media only screen and (min-width: 992px) {
  .astro-section {
    background-color: rgba(245, 248, 255, 1);
    height: 460px;
    width: 100%;
  }
  .astro-container {
    display: flex;
    width: 100%;
    margin: 0;
  }
  .astro-text {
    margin-top: 120px;
    margin-left: 120px;
    text-align: left;
  }
  .astro-head {
    color: rgb(17, 51, 85);
    font-weight: 800;
  }

  .astro-img {
    display: block;
  }
  h2 {
    line-height: 1.3;
    color: rgb(var(--gray100));
    font-size: 32px;
    font-weight: 500;
    color: rgba(10, 11, 13, 1);
    text-align: left;
  }
  p {
    font-size: 14px;
    color: rgb(17, 51, 85);
    line-height: 1.6;
    font-size: 16px;
    text-align: left;
    font-weight: 400;
    margin-top: 10px;
    width: 100%;
  }
  button {
    width: 140px;
    height: 40px;
    margin: 15px 0 0;
    font-size: 16px;
  }
}
</style>