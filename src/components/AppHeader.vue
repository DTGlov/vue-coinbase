<template>
  <div class="con">
    <header>
      <nav id="nav" @mouseleave="hideLinks">
        <router-link class="link" to="/">
          <img src="../assets/coinlogo.svg" alt="coinbase-logo" />
        </router-link>
        <ul class="link-wrapper">
          <li>
            <router-link to="/prices">Prices</router-link>
          </li>
          <li @mouseover="toggleShowLearn">
            <router-link to="/">Learn</router-link>
          </li>
          <li @mouseover="toggleShowIndi">
            <router-link to="/">Individuals</router-link>
          </li>
          <li @mouseover="toggleShowBus">
            <router-link to="/">Businesses</router-link>
          </li>
          <li><router-link to="/">Developers</router-link></li>
          <li><router-link to="/">Company</router-link></li>
        </ul>
        <div class="sign">
          <p>Sign in</p>
          <button class="nav-btn">Get Started</button>
        </div>
        <i
          class="fas fa-bars fa-lg"
          @click="toggleShow"
          v-if="show === false"
        ></i>
        <i
          @click="toggleShow"
          v-if="show === true"
          class="fas fa-times fa-lg"
        ></i>
      </nav>
    </header>
    <div v-if="showLearn" class="learn-section">
      <div class="learn-container">
        <div class="learn-con">
          <div class="chev">
            <i class="fas fa-chevron-right fa-sm"></i>
            <p>Tips and Tutorials</p>
          </div>
          <div>
            <i class="fas fa-chevron-right fa-sm"></i>
            <p>Crypto basics</p>
          </div>
          <div>
            <i class="fas fa-chevron-right fa-sm"></i>
            <p>Market updates</p>
          </div>
        </div>
        <div>
          <p class="cryt">
            Crypto questions, answered Guides and explainers for your crypto
            questions
          </p>
          <p class="articles">See all articles</p>
        </div>
      </div>
    </div>
    <div v-if="showIndi" class="indi-section">
      <div class="indi-container">
        <div class="items">
          <div class="indimag">
            <img src="../assets/coinbase.svg" alt="" />
            <div>
              <h3>Buy and sell</h3>
              <p>Buy,sell and use crypto</p>
            </div>
          </div>
          <div class="indimag">
            <img src="../assets/earn.svg" alt="" />
            <div>
              <h3>Earn</h3>
              <p>Learn and Earn crypto</p>
            </div>
          </div>
          <div class="indimag">
            <img src="../assets/pri.svg" alt="" />
            <div>
              <h3>Private Client</h3>
              <p>For trusts, family offices, UHNWIs</p>
            </div>
          </div>
        </div>
        <div class="items2">
          <div class="indimag">
            <img src="../assets/wallet.svg" alt="" />
            <div>
              <h3>Wallet</h3>
              <p>The best self-hosted crypto wallet</p>
            </div>
          </div>
          <div class="indimag">
            <img src="../assets/card.svg" alt="" />
            <div>
              <h3>Card</h3>
              <p>Spend crypto, earn crypto rewards</p>
            </div>
          </div>
          <div class="indimag">
            <img src="../assets/borrow.svg" alt="" />
            <div>
              <h3>Borrow</h3>
              <p>Borrow cash using Bitcoin as collateral</p>
            </div>
          </div>
        </div>
        <div class="items">
          <p class="cryt">
            Crypto questions, answered Guides and explainers for your crypto
            questions
          </p>
          <p class="articles">See all articles</p>
        </div>
      </div>
    </div>
    <div v-if="showBusiness" class="indi-section">
      <div class="indi-container">
        <div class="items">
          <div class="indimag">
            <img src="../assets/prime.svg" alt="" />
            <div>
              <h3>Prime</h3>
              <p>The prime brokerage platform</p>
            </div>
          </div>
          <div class="indimag">
            <img src="../assets/custody.svg" alt="" />
            <div>
              <h3>Custody</h3>
              <p>Institutional-grade offline storage</p>
            </div>
          </div>
          <div class="indimag">
            <img src="../assets/exchange.svg" alt="" />
            <div>
              <h3>Exchange</h3>
              <p>Direct access to our exchange</p>
            </div>
          </div>
        </div>
        <div class="items2">
          <div class="indimag">
            <img src="../assets/commerce.svg" alt="" />
            <div>
              <h3>Commerce</h3>
              <p>Accept crypto from anyone</p>
            </div>
          </div>
          <div class="indimag">
            <img src="../assets/asset.svg" alt="" />
            <div>
              <h3>Asset Hub</h3>
              <p>List your assets on Coinbase</p>
            </div>
          </div>
          <div class="indimag">
            <img src="../assets/analytics.svg" alt="" />
            <div>
              <h3>Analytics</h3>
              <p>Power your crypto compliance</p>
            </div>
          </div>
        </div>
        <div class="items">
          <p class="cryt">
            Built for businesses and institutions Crypto solutions for
            institutional investors
          </p>
          <p class="articles">See all articles</p>
        </div>
      </div>
    </div>
    <div class="drop-section" v-if="show">
      <div class="drop-container">
        <div class="drop">
          <p>Prices</p>
        </div>
        <div class="drop">
          <p>Learn</p>
          <i class="fas fa-chevron-down"></i>
        </div>
        <div class="drop">
          <p>Individuals</p>
          <i class="fas fa-chevron-down"></i>
        </div>
        <div class="drop">
          <p>Businesses</p>
          <i class="fas fa-chevron-down"></i>
        </div>
        <div class="drop">
          <p>Developers</p>
          <i class="fas fa-chevron-down"></i>
        </div>
        <div class="drop">
          <p>Company</p>
          <i class="fas fa-chevron-down"></i>
        </div>
        <div class="btn-container">
          <button class="start-btn">Get Started</button>
          <button class="sign-btn">Sign in</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: false,
      showLearn: false,
      showIndi: false,
      showBusiness: false,
    };
  },
  methods: {
    toggleShow() {
      this.show = !this.show;
    },
    toggleShowLearn() {
      this.showLearn = true;
      this.showIndi = false;
      this.showBusiness = false;
    },
    toggleShowIndi() {
      this.showIndi = true;
      this.showBusiness = false;
      this.showLearn = false;
    },
    toggleShowBus() {
      this.showBusiness = true;
      this.showIndi = false;
      this.showLearn = false;
    },
    hideLinks() {
      this.showLearn = false;
      this.showIndi = false;
      this.showBusiness = false;
    },
  },
};
</script>

<style scoped>
.con {
  position: -webkit-sticky;
  position: sticky;
  top: 0;
  z-index: 1;
  width: 100%;
}
header {
  height: 60px;
  background-color: white;
  border-bottom: 1px solid rgb(236, 239, 241);
}

#nav {
  display: flex;
  width: 90%;
  height: 60px;
  margin: 0 auto;
  align-items: center;
}

#nav a {
  text-decoration: none;
  color: rgb(5, 15, 25);
  font-weight: 900;
}
.drop-section {
  background: white;
  padding-top: 40px;
  position: fixed;
  left: 0;
  right: 0;
  top: 60px;
  height: 100%;
  z-index: 1;
}
.drop-container {
  width: 90%;
  margin: 0 auto;
}
.drop {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 30px;
}

.link {
  display: block;
  width: 100%;
}

img {
  width: 200%;
}
.link-wrapper {
  display: none;
}
.fa-bars,
.fa-times {
  margin-left: 20px;
  color: grey;
  cursor: pointer;
}

.link-wrapper li {
  list-style-type: none;
  margin-left: 20px;
  font-size: 15px;
  height: 56px;
  display: flex;
  align-items: center;
  border-bottom: 4px solid white;
}

li:hover {
  border-bottom: 4px solid rgb(0, 82, 255);
}
.sign {
  margin-left: 100px;
  display: flex;
  align-items: center;
}
.sign p {
  display: none;
}

.nav-btn {
  display: block;
  font-family: inherit;
  border: 1px solid rgb(0, 82, 255);
  background-color: rgb(0, 82, 255);
  font-weight: 900;
  line-height: 14px;
  width: 120px;
  height: 40px;
  border-radius: 4px;
  color: white;
  margin-left: 25px;
}
.btn-container {
  display: flex;
  flex-direction: column;
}

.start-btn {
  display: block;
  border: none;
  background-color: rgb(0, 82, 255);
  border-radius: 4px;
  color: white;
  height: 50px;
  font-family: inherit;
}
.sign-btn {
  display: block;
  font-family: inherit;
  border: 2px solid rgb(0, 82, 255);
  background-color: white;
  height: 50px;
  margin-top: 10px;
  border-radius: 4px;
  color: rgb(0, 82, 255);
}
.learn-section,
.indi-section {
  display: none;
}
@media only screen and (min-width: 992px) {
  .con {
    position: -webkit-sticky;
    position: sticky;
    top: 0;
    z-index: 1;
    width: 100%;
  }
  header {
    height: 60px;
    background-color: white;
    border-bottom: 1px solid rgb(236, 239, 241);
  }
  .drop-section {
    display: none;
  }

  .fa-bars {
    display: none;
  }
  #nav {
    display: flex;
    width: 90%;
    height: 60px;
    margin: 0 auto;
    align-items: center;
  }

  #nav a {
    text-decoration: none;
    color: rgb(5, 15, 25);
    font-weight: 900;
  }

  .link {
    width: 20%;
  }

  img {
    width: 50%;
  }
  .link-wrapper {
    display: flex;
    margin-left: 120px;
  }

  .link-wrapper li {
    list-style-type: none;
    margin-left: 20px;
    font-size: 15px;
    height: 56px;
    display: flex;
    align-items: center;
    border-bottom: 4px solid white;
  }

  li:hover {
    border-bottom: 4px solid rgb(0, 82, 255);
  }
  .sign {
    margin-left: 100px;
    display: flex;
    align-items: center;
  }
  .sign p {
    display: block;
    font-size: 15px;
    font-weight: 900;
    color: rgb(5, 15, 25);
  }

  button {
    display: block;
    font-family: inherit;
    border: 1px solid rgb(0, 82, 255);
    background-color: rgb(0, 82, 255);
    font-weight: 900;
    line-height: 14px;
    width: 120px;
    height: 40px;
    border-radius: 4px;
    color: white;
    margin-left: 25px;
  }
  .learn-section {
    display: flex;
    background-color: white;
    height: 180px;
    align-items: center;
    position: absolute;
    right: 0;
    left: 0;
    box-shadow: -1px 2px 5px 0px rgba(227, 218, 218, 0.67);
    -webkit-box-shadow: -1px 2px 5px 0px rgba(227, 218, 218, 0.67);
    -moz-box-shadow: -1px 2px 5px 0px rgba(227, 218, 218, 0.67);
  }
  .learn-container {
    display: flex;
    width: 50%;
    margin-left: 500px;
  }
  .learn-con div {
    display: flex;
    margin-right: 100px;
    margin-bottom: 20px;
    align-items: center;
  }

  .cryt {
    width: 250px;
    line-height: 1.4;
  }
  .fa-chevron-right {
    margin-right: 10px;
  }
  .articles {
    color: rgb(0, 82, 255);
    margin-top: 10px;
    font-size: 18px;
  }
  .indi-section {
    display: flex;
    background-color: white;
    height: 220px;
    align-items: center;
    position: absolute;
    right: 0;
    left: 0;
    box-shadow: -1px 2px 5px 0px rgba(227, 218, 218, 0.67);
    -webkit-box-shadow: -1px 2px 5px 0px rgba(227, 218, 218, 0.67);
    -moz-box-shadow: -1px 2px 5px 0px rgba(227, 218, 218, 0.67);
  }
  .indi-container {
    display: flex;
    margin: 0 auto;
    width: 80%;
    justify-content: space-between;
  }
  .indimag {
    display: flex;
    margin-bottom: 10px;
  }
  .items {
    width: 30%;
  }
  .items2 {
    width: 35%;
  }
  .indimag img {
    width: 12%;
    margin-right: 10px;
  }
  .indimag p {
    color: rgb(116, 115, 115);
    font-weight: 400;
  }
  .indimag h3 {
    font-size: 16px;
  }
}
</style>