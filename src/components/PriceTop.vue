<template>
  <div class="top-section">
    <div class="top-container">
      <div class="market-input">
        <div class="text-con">
          <p class="pass">In the past 24hrs</p>
          <p class="market">Market is down <span class="down">0.86%</span></p>
        </div>
        <div>
          <input type="text" placeholder="Search" />
        </div>
      </div>
      <div class="card-container">
        <div v-for="card in cardInfo" :key="card.name" class="card">
          <p>{{ card.status }}</p>
          <img :src="require(`@/assets/${card.img}`)" alt="" />
          <p class="card-name">{{ card.name }}</p>
          <p class="card-info">{{ card.info }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PriceTop",
  data() {
    return {
      cardInfo: [
        {
          status: "Top gainer",
          img: "coti.png",
          name: "COTI",
          info: "+31.01% price change",
        },
        {
          status: "New listing",
          img: "dsocial.png",
          name: "Decentralized Social",
          info: "Added Dec 13",
        },
        {
          status: "Most visited",
          img: "gitcoin.png",
          name: "Gitcoin",
          info: "+3.2323 views",
        },
        {
          status: "Most traded",
          img: "bitcoin.png",
          name: "Bitcoin",
          info: "USD 123 volume(24h)",
        },
        {
          status: "Free crypto",
          img: "stellar.png",
          name: "Stellar Lumens",
          info: "Earn $10",
        },
      ],
    };
  },
};
</script>

<style scoped>
.top-section {
  padding: 25px 0;
}
.top-container {
  width: 85%;
  margin: 0 auto;
}
.card-container {
  height: 200px;
  /* background-color: gainsboro; */
}
.text-con {
  margin-bottom: 15px;
}
.pass {
  font-weight: 600;
  color: grey;
}
.market {
  font-size: 24px;
  font-weight: 600;
}
.market-input {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
input {
  width: 600px;
  height: 40px;
  font-family: inherit;
  padding: 15px;
  font-size: 16px;
}
.down {
  color: rgb(211, 16, 16);
}
.card-container {
  display: flex;
}
.card {
  width: 25%;
  /* background: aqua; */
  margin: 10px;
  border: 1px solid gainsboro;
  border-radius: 10px;
  padding: 15px;
}
.card img {
  width: 20%;
  margin-top: 15px;
}
.card-name {
  margin-top: 10px;
}
.card-info {
  margin-top: 10px;
}
</style>