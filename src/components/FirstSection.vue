<template>
  <div class="first-section">
    <div class="first-container">
      <div class="tabl">
        <table id="crypto-table">
          <thead class="desk">
            <tr>
              <th>#</th>
              <th>Name</th>
              <th>Price</th>
              <th>Change</th>
              <th>Chart</th>
              <th>Trade</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(crypto, id) in getCrypto.slice(0, 4)" :key="crypto.id">
              <td class="id">{{ id + 1 }}</td>
              <td>
                <div class="tab">
                  <figure>
                    <img :src="crypto.image" alt="" class="crypt-img" />
                  </figure>

                  <p>{{ crypto.name }}</p>
                  <p class="symbol">{{ crypto.symbol.toUpperCase() }}</p>
                </div>
              </td>
              <td class="price">USD {{ crypto.current_price }}</td>
              <td>
                <div
                  class="percent"
                  :class="{ red: crypto.price_change_percentage_24h < 0 }"
                >
                  <p>{{ crypto.price_change_percentage_24h.toFixed(2) }}</p>
                  <i class="fas fa-percent fa-sm"></i>
                </div>
              </td>
              <td>
                <svg
                  :class="{ sparkred: crypto.price_change_percentage_24h < 0 }"
                  class="sparkline"
                  width="100"
                  height="30"
                  stroke-width="2"
                ></svg>
              </td>
              <td><button class="trade-btn">Buy</button></td>
            </tr>
          </tbody>
        </table>
      </div>

      <!-- mobile table -->
      <div class="mobi">
        <div
          class="mobi-con"
          v-for="crypto in getCrypto.slice(0, 4)"
          :key="crypto.id"
        >
          <div class="mobi-left">
            <figure>
              <img :src="crypto.image" alt="" />
            </figure>
            <div class="mobi-cry">
              <p>{{ crypto.name }}</p>
              <p class="symbol">{{ crypto.symbol.toUpperCase() }}</p>
            </div>
          </div>
          <div class="mobi-rigth">
            <p class="cash">USD {{ crypto.current_price }}</p>
            <div
              class="percent pp"
              :class="{ red: crypto.price_change_percentage_24h < 0 }"
            >
              <p>
                {{ crypto.price_change_percentage_24h.toFixed(2) }}
              </p>
              <i class="fas fa-percent fa-sm"></i>
            </div>
          </div>
        </div>
      </div>
      <!-- end of mobile table -->
      <div class="base">
        <div class="left">
          <div class="astro-text">
            <h2 class="astro-head">Earn up to $10 worth of crypto</h2>
            <p class="astro-para">
              Discover how specific cryptocurrencies work — and get a bit of
              each crypto to try out for yourself.
            </p>
            <button class="earn-btn">Start earning</button>
          </div>
        </div>
        <div class="right">
          <div class="right-con">
            <div class="crypto">
              <img src="../assets/mon.svg" alt="" />
              <h3>Stellar Lumens <span>XLM</span></h3>
            </div>
            <p class="earn">Earn $10 XLM</p>
          </div>
          <div class="view">
            <p>View more</p>
            <i class="fas fa-chevron-right"></i>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapActions, mapGetters } from "vuex";
import sparkline from "@fnando/sparkline";

export default {
  name: "FirstSection",
  methods: {
    ...mapActions(["fetchCrypto"]),
  },
  mounted() {
    this.fetchCrypto();
  },
  beforeUpdate() {
    this.$nextTick(function () {
      function randNumbers() {
        let numbers = [];

        for (let i = 0; i < 20; i += 1) {
          numbers.push(Math.random() * 50);
        }
        return numbers;
      }
      document.querySelectorAll(".sparkline").forEach((svg) => {
        sparkline(svg, randNumbers());
      });
    });
  },
  computed: {
    ...mapGetters(["getCrypto"]),
  },
};
</script>

<style scoped>
.first-section {
  padding-bottom: 60px;
}
.first-container {
  width: 85%;
  margin: 0 auto;
}
.astro-text {
  /* margin-top: 35px; */
  text-align: center;
}
.tabl {
  display: none;
}
.astro-head {
  line-height: 1.3;
  color: rgba(10, 11, 13, 1);
  font-size: 32px;
  font-weight: 500;
  text-align: center;
  width: 280px;
  margin: 0 auto;
}
.astro-para {
  font-size: 15px;
  line-height: 1.6;
  font-weight: 400;
  color: rgba(10, 11, 13, 1);
  margin-top: 10px;
  width: 260px;
  margin: 10px auto;
}
.earn-btn {
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
.right-con {
  display: flex;
  align-items: center;
  border: 1px solid gainsboro;
  margin-top: 20px;
}
.crypto {
  display: flex;
  padding: 10px;
}
.crypto h3 {
  margin-left: 20px;
  width: 100px;
  font-size: 22px;
}
.earn {
  margin-left: 40px;
  color: rgba(9, 133, 8, 0.8);
  font-weight: 700;
  font-size: 14px;
}
span {
  display: none;
}
.view {
  display: flex;
  margin-top: 15px;
  align-items: center;
  color: rgb(0, 82, 255);
}
.fas {
  margin-left: 5px;
}
.mobi {
  padding-top: -50px;
  padding-bottom: 20px;
}
.mobi-con {
  display: flex;
  border-top: 1px solid gainsboro;
  width: 117%;
  margin-left: -26px;
  padding: 15px;
}
.mobi-left {
  display: flex;
}
.mobi-left figure {
  width: 15%;
}
.mobi-left img {
  width: 100%;
}
.mobi-cry {
  margin-left: 15px;
}

.mobi-right {
  display: flex;
  text-align: right;
}
.cash {
  width: 100px;
}
.percent {
  display: flex;
  align-items: center;
}
.pp {
  color: #098551;
}
@media only screen and (min-width: 992px) {
  .mobi {
    display: none;
  }
  .first-section {
    padding-bottom: 80px;
  }
  .astro-text {
    width: 400px;
  }
  .astro-head {
    line-height: 1.3;
    color: rgb(var(--gray100));
    font-size: 32px;
    font-weight: 800;
    color: rgba(10, 11, 13, 1);
    text-align: left;
    margin: 0;
    width: 100%;
  }
  .astro-para {
    font-size: 14px;
    color: rgb(17, 51, 85);
    line-height: 1.6;
    font-size: 16px;
    text-align: left;
    font-weight: 400;
    margin-top: 10px;
    width: 100%;
  }
  .earn-btn {
    width: 140px;
    height: 40px;
    margin: 15px 0 0;
    font-size: 16px;
  }
  .base {
    margin-top: 30px;
    display: flex;
    justify-content: space-between;
  }
  .left {
    width: 40%;
  }
  .right {
    width: 50%;
    display: flex;
    flex-direction: column;
    margin-top: 20px;
  }
  .right-con {
    display: flex;
    align-items: center;
    border: none;
    margin-top: 0;
  }
  .crypto {
    display: flex;
    align-items: center;
    padding: 0;
  }
  .crypto h3 {
    margin-left: 20px;
    width: 220px;
    font-size: 22px;
  }
  .earn {
    margin-left: 190px;
    color: rgba(9, 133, 8, 0.8);
    font-weight: 700;
    font-size: 16px;
  }
  .view {
    display: flex;
    align-items: center;
    margin-top: 30px;
    color: rgb(0, 82, 255);
    font-size: 18px;
  }
  .fas {
    margin-left: 5px;
  }
  span {
    display: inline;
  }
  #crypto-table {
    font-family: inherit;
    border-collapse: collapse;
    width: 100%;
    border: 1px solid gainsboro;
    border-radius: 4px;
  }
  .tabl {
    display: block;
  }

  #crypto-table td,
  #crypto-table th {
    /* border: 1px solid #ddd; */
    padding: 15px;
  }

  #crypto-table tr:nth-child(even) {
    /* background-color: #f2f2f2; */
  }

  #crypto-table tr:hover {
    background-color: rgb(247, 247, 247);
  }

  #crypto-table th {
    padding-top: 12px;
    padding-bottom: 12px;
    text-align: left;
    /* background-color: #04aa6d; */
    /* color: white; */
  }
  figure {
    width: 7%;
  }
  .crypt-img {
    width: 100%;
  }
  th {
    color: grey;
    font-weight: 200;
    font-size: 16px;
  }
  tr {
    border-bottom: 1px solid gainsboro;
  }
  .tab {
    display: flex;
    align-items: center;
  }
  .tab p {
    margin-left: 10px;
    font-size: 20px;
  }
  .id {
    color: grey;
  }

  .symbol {
    color: grey;
    font-weight: 400;
  }
  .percent {
    display: flex;
    align-items: center;
    color: #098551;
  }
  .percent p {
    font-size: 18px;
  }
  .price {
    font-size: 18px;
    font-weight: 400;
  }
  .trade-btn {
    border: none;
    display: block;
    background-color: #098551;
    color: white;
    font-family: inherit;
    font-weight: 600;
    font-size: 16px;
    border-radius: 4px;
    width: 60px;
    height: 30px;
  }
}
.sparkline {
  stroke: rgb(155, 147, 147);
  fill: none;
}
.sparkred {
  stroke: red;
  fill: none;
}
.red {
  color: red;
}
</style>