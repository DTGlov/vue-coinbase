<template>
  <div class="nav">
    <div class="brand">
      <router-link to="/"><img src="../assets/logo.svg" alt /></router-link>
    </div>
    <ul :class="`list nav-links ${expanded}`">
      <li class="nav-item" @click="toggleNav">
        <router-link class="link" to="/prices"><h4>Prices</h4></router-link>
      </li>
      <li
        class="nav-item"
        @click="collapse"
        @mouseover="collapse"
        @mouseout="collapse"
      >
        <h4 data-dd="dd1">
          Learn
          <span class="drop-icon"
            ><img src="../assets/chevron-down.svg" alt="" data-dd="dd1"
          /></span>
        </h4>
        <ul class="dropdown list" id="dd1">
          <ul class="col1 list">
            <li>
              <span class=""
                ><img
                  src="../assets/chevron-right.svg"
                  alt=""
                  data-dd="dd3" /></span
              >Tips & Tutorials
            </li>
            <li>
              <span class=""
                ><img
                  src="../assets/chevron-right.svg"
                  alt=""
                  data-dd="dd3" /></span
              >Crypto basics
            </li>
            <li>
              <span class=""
                ><img
                  src="../assets/chevron-right.svg"
                  alt=""
                  data-dd="dd3" /></span
              >Market Updates
            </li>
          </ul>
          <li class="col2">
            <h5>Crypto questions, answered</h5>
            <p>Guides and explainers for your crypto questions</p>
            <a href="sad">See all articles</a>
          </li>
        </ul>
      </li>
      <li
        class="nav-item"
        @click="collapse"
        @mouseover="collapse"
        @mouseout="collapse"
      >
        <h4 data-dd="dd2">
          Individuals
          <span class="drop-icon"
            ><img src="../assets/chevron-down.svg" alt="" data-dd="dd2"
          /></span>
        </h4>
        <ul class="dropdown list" id="dd2">
          <div class="col1">
            <li>
              <div class="icons">
                <img src="../assets/coinbase-icon2.svg" alt="" />
              </div>
              <div>
                <h5>Buy and sell</h5>
                <p>Buy, sell and use crypto</p>
              </div>
            </li>
            <li>
              <div class="icons">
                <img src="../assets/round-wallet.svg" alt="" />
              </div>
              <div>
                <h5>Wallet</h5>
                <p>The best self-hosted crypto wallet</p>
              </div>
            </li>
            <li>
              <div class="icons">
                <img src="../assets/earn-icon.svg" alt="" />
              </div>
              <div>
                <h5>Earn</h5>
                <p>Learn and earn crypto</p>
              </div>
            </li>
            <li>
              <div class="icons">
                <img src="../assets/round-card.svg" alt="" />
              </div>
              <div>
                <h5>Card</h5>
                <p>Send crypto, earn crypto rewards</p>
              </div>
            </li>
            <li>
              <div class="icons">
                <img src="../assets/diamond.svg" alt="" />
              </div>
              <div>
                <h5>Buy and sell</h5>
                <p>For trusts, family offices and UHNWIs</p>
              </div>
            </li>
            <li>
              <div class="icons">
                <img src="../assets/Borrow_Round.svg" alt="" />
              </div>
              <div>
                <h5>Borrow</h5>
                <p>Borrow cash using Bitcoin as collateral</p>
              </div>
            </li>
          </div>
          <div class="col2">
            <h5>Crypto tools for everyone</h5>
            <p>
              Buy, sell, and spend crypto on the world's most trusted crypto
              exchange
            </p>
            <a href="sad">See all products</a>
          </div>
        </ul>
      </li>
      <li
        class="nav-item"
        @click="collapse"
        @mouseover="collapse"
        @mouseout="collapse"
      >
        <h4 data-dd="dd3">
          Businesses
          <span class="drop-icon"
            ><img src="../assets/chevron-down.svg" alt="" data-dd="dd3"
          /></span>
        </h4>
        <ul class="dropdown list" id="dd3">
          <div class="col1">
            <li>
              <div class="icons">
                <img src="../assets/prime-icon.svg" alt="" />
              </div>
              <div>
                <h5>Prime</h5>
                <p>The prime brokerage platform</p>
              </div>
            </li>
            <li>
              <div class="icons">
                <img src="../assets/commerce-icon.svg" alt="" />
              </div>
              <div>
                <h5>Commerce</h5>
                <p>Accept crypto from anyone</p>
              </div>
            </li>
            <li>
              <div class="icons">
                <img src="../assets/custody-icon.svg" alt="" />
              </div>
              <div>
                <h5>Custody</h5>
                <p>Institutional-grade offline storage</p>
              </div>
            </li>
            <li>
              <div class="icons">
                <img src="../assets/asset-hub-icon.svg" alt="" />
              </div>
              <div>
                <h5>Asset Hub</h5>
                <p>List your asset on Coinbase</p>
              </div>
            </li>
            <li>
              <div class="icons">
                <img src="../assets/exchange.svg" alt="" />
              </div>
              <div>
                <h5>Exchange</h5>
                <p>Direct access to our exchange</p>
              </div>
            </li>
            <li>
              <div class="icons">
                <img src="../assets/round_analytics.svg" alt="" />
              </div>
              <div>
                <h5>Analytics</h5>
                <p>Power your crypto compliance</p>
              </div>
            </li>
          </div>
          <div class="col2">
            <h5>Built for businesses and institutions</h5>
            <p>
              Crypto solutions for institutional investors, family offices, and
              businesses
            </p>
            <a href="sad">See all products</a>
          </div>
        </ul>
      </li>
      <li
        class="nav-item"
        @click="collapse"
        @mouseover="collapse"
        @mouseout="collapse"
      >
        <h4 data-dd="dd4">
          Developers
          <span class="drop-icon"
            ><img src="../assets/chevron-down.svg" alt="" data-dd="dd4"
          /></span>
        </h4>
        <ul class="dropdown list" id="dd4">
          <div class="col1">
            <li>
              <div class="">
                <img src="../assets/chevron-right.svg" width="8" alt="" />
              </div>
              <div>
                <h5>Connect</h5>
                <p>Enable users to buy, sell, and store crypto</p>
              </div>
            </li>
            <li>
              <div class="">
                <img src="../assets/chevron-right.svg" width="8" alt="" />
              </div>
              <div>
                <h5>Bison Trails</h5>
                <p>Pioneering blockchain infrastructure</p>
              </div>
            </li>
            <li>
              <div class="">
                <img src="../assets/chevron-right.svg" width="8" alt="" />
              </div>
              <div>
                <h5>Commerce</h5>
                <p>Accept crypto from anyone</p>
              </div>
            </li>
            <li>
              <div class="">
                <img src="../assets/chevron-right.svg" width="8" alt="" />
              </div>
              <div>
                <h5>WalletLink</h5>
                <p>Link your DApp to mobile wallets</p>
              </div>
            </li>
            <li>
              <div class="">
                <img src="../assets/chevron-right.svg" width="8" alt="" />
              </div>
              <div>
                <h5>Pro</h5>
                <p>Programmatically manage crypto</p>
              </div>
            </li>
            <li>
              <div class="">
                <img src="../assets/chevron-right.svg" width="8" alt="" />
              </div>
              <div>
                <h5>Rosetta</h5>
                <p>Integrate your blockchain everywhere</p>
              </div>
            </li>
          </div>
          <div class="col2">
            <h5>Build with Coinbase Cloud</h5>
            <p>Tools and APIs for developers building with crypto</p>
            <a href="sad">Explore Coinbase Cloud</a>
          </div>
        </ul>
      </li>
      <li
        class="nav-item"
        @click="collapse"
        @mouseover="collapse"
        @mouseout="collapse"
      >
        <h4 data-dd="dd5">
          Company
          <span class="drop-icon"
            ><img src="../assets/chevron-down.svg" alt="" data-dd="dd5"
          /></span>
        </h4>
        <ul class="dropdown list" id="dd5">
          <div class="col1">
            <li>
              <div class="">
                <img src="../assets/chevron-right.svg" alt="" />
              </div>
              <div>
                <h5>About</h5>
              </div>
            </li>
            <li>
              <div class="">
                <img src="../assets/chevron-right.svg" alt="" />
              </div>
              <div>
                <h5>Careers</h5>
              </div>
            </li>
            <li>
              <div class="">
                <img src="../assets/chevron-right.svg" alt="" />
              </div>
              <div>
                <h5>Affiliates</h5>
              </div>
            </li>
            <li>
              <div class="">
                <img src="../assets/chevron-right.svg" alt="" />
              </div>
              <div>
                <h5>Support</h5>
              </div>
            </li>
            <li>
              <div class="">
                <img src="../assets/chevron-right.svg" alt="" />
              </div>
              <div>
                <h5>BLog</h5>
              </div>
            </li>
          </div>
          <div class="col2">
            <h5>Learn all about Coinbase</h5>
            <p>We're building an open financial system for the world.</p>
          </div>
        </ul>
      </li>
      <div class="btns">
        <button class="btn btn-primary">Get started</button>
        <button class="btn btn-secondary">Sign in</button>
      </div>
    </ul>
    <div class="buttons">
      <button class="btn btn-secondary">Sign in</button>
      <button class="btn btn-primary">Get started</button>
    </div>
    <div @click="toggleNav" class="nav-toggle">
      <img :src="require(`../assets/${toggleIcon}.svg`)" alt />
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return { toggled: false };
  },
  computed: {
    expanded() {
      return this.toggled ? "show" : "";
    },
    toggleIcon() {
      return this.toggled ? "x" : "hamburger";
    },
  },
  methods: {
    toggleNav() {
      this.toggled = !this.toggled;
    },
    collapse(e) {
      const width =
        window.innerWidth ||
        document.documentElement.clientWidth ||
        document.body.clientWidth;
      if (width <= 950 && e.type !== "click") {
        return;
      }

      let dd = document.getElementById(e.target.getAttribute("data-dd"));
      if (!dd) {
        return;
      }
      if (dd.classList.contains("show")) {
        dd.classList.remove("show");
      } else {
        dd.classList.add("show");
      }
      let dropdowns = document.getElementsByClassName("dropdown");
      Array.from(dropdowns).forEach((el) => {
        if (el.id !== dd.id) {
          el.classList.remove("show");
        }
      });
    },
  },
};
</script>

<style scoped>
.link {
  color: var(--text);
  text-decoration: none;
}
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: fixed;
  width: 100%;
  border-bottom: 1px solid rgb(236, 239, 241);
  padding: 0 90px;
  background-color: white;
  z-index: 2;
}
.nav-links {
  display: flex;
  gap: 40px;
  background-color: white;
}
.nav-links h4 {
  font-size: 14px;
  font-weight: 500;
  padding: 20px 0;
  border-bottom: 3px solid transparent;
  line-height: 16px;
}
.buttons {
  display: flex;
  gap: 5px;
}
.buttons .btn {
  padding: 10px 12px;
  font-size: 14px;
  line-height: 14px;
}
.buttons :first-child {
  border: none;
  color: var(--text);
}
.brand {
  width: 112px;
}
.drop-icon {
  width: 20px;
  display: none;
}
/* .drop-icon img {
  width: 20px;
} */
.nav-toggle {
  width: 30px;
  display: none;
  cursor: pointer;
}

.nav-item h4:hover {
  border-bottom-color: var(--primary);
}
.dropdown {
  display: none;
  /* display: flex; */
  background-color: white;
}
.dropdown.show {
  display: flex;
  position: absolute;
  top: 70px;
  left: 0;
  padding: 40px 45px;
  width: 100%;
  justify-content: center;
  gap: 80px;
  font-size: 16px;
  border-bottom: 1px solid rgb(236, 239, 241);
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.dropdown a {
  color: var(--primary);
  font-weight: 500;
  text-decoration: none;
  font-size: 16px;
}
.dropdown .col1,
.dropdown .col2,
.dropdown h5 {
  font-size: 16px;
}
.dropdown h5 {
  font-weight: 500;
  line-height: 16px;
}
.dropdown p {
  line-height: 20px;
}
.dropdown .drop-icon {
  display: inline;
  width: 18px;
}
.drop-icon img {
  width: 100%;
}
.dropdown .icons {
  width: 40px;
  height: 40px;
  box-shadow: 0 2px 2px 2px rgba(0, 0, 0, 0.1);
  border-radius: 100%;
}
.dropdown .icons img {
  width: 40px;
}

#dd1 .col1 li {
  display: flex;
  gap: 20px;
}
#dd1 .col1 {
  font-weight: 500;
  display: flex;
  flex-direction: column;
  gap: 20px;
}
#dd1 .col2 {
  max-width: 300px;
  line-height: 24px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
#dd2 .col1,
#dd5 .col1,
#dd3 .col1,
#dd4 .col1 {
  display: grid;
  grid-template-columns: 1fr 1fr;
  row-gap: 20px;
  column-gap: 30px;
}
#dd2 .col1 li,
#dd5 .col1 li,
#dd4 .col1 li,
#dd3 .col1 li {
  display: flex;
  gap: 15px;
}
#dd2 .col1 p,
#dd5 .col1 p,
#dd4 .col1 p,
#dd3 .col1 p {
  color: rgba(17, 51, 83, 0.6);
  line-height: 20px;
  margin-top: 4px;
}
#dd2 .col2,
#dd5 .col2,
#dd4 .col2,
#dd3 .col2 {
  max-width: 310px;
  line-height: 24px;
  display: flex;
  flex-direction: column;
}
#dd2 .col2 p,
#dd5 .col2 p,
#dd4 .col2 p,
#dd3 .col2 p {
  margin: 10px 0 20px;
}
#dd4 img,
#dd5 img,
#dd1 img {
  width: 8px;
  height: 11px;
}
.btns {
  display: none;
}

@media screen and (max-width: 950px) {
  .nav {
    padding: 10px 24px;
  }
  .nav-links {
    position: absolute;
    top: 58px;
    left: 0;
    flex-direction: column;
    padding: 5px 0;
    gap: 0;
    background-color: white;
    width: 100%;
    height: calc(100vh - 100px);
    overflow-y: scroll;
    display: none;
  }
  .nav-links.show {
    display: flex;
  }
  .nav-item:hover {
    background-color: rgba(0, 81, 255, 0.05);
  }
  .nav-links h4 {
    font-size: 16px;
    padding: 20px 24px;
    display: flex;
    justify-content: space-between;
  }
  .buttons {
    margin-left: auto;
    margin-right: 50px;
  }

  .buttons :first-child {
    display: none;
  }

  .drop-icon {
    display: inline;
  }
  .drop-icon img {
    width: 12px;
    height: 8px;
  }

  .nav-toggle {
    width: 30px;
    display: inline-block;
  }

  .nav-item h4:hover {
    border-bottom-color: transparent;
  }
  .dropdown {
    display: none;
    background-color: white;
  }
  .dropdown.show {
    display: flex;
    flex-direction: column;
    position: initial;
    padding: 20px 24px;
    justify-content: flex-start;
    gap: 17px;
    box-shadow: none;
    background: rgb(241, 243, 245);
    border-top: 1px solid rgb(255, 255, 255);
    border-bottom: 1px solid rgb(255, 255, 255);
  }
  .dropdown .col2 p,
  .dropdown .col2 h5 {
    display: none;
  }
  .dropdown h5 {
    font-weight: 400;
  }
  .dropdown a {
    color: var(--text);
    font-weight: 400;
  }

  .dropdown .drop-icon {
    display: none;
  }
  .dropdown .icons {
    display: none;
  }

  .dropdown img {
    display: none;
  }

  #dd1 .col1 li {
    gap: 0;
  }
  #dd1 .col1 {
    font-weight: 400;
    gap: 34px;
  }
  #dd1 .col2 {
    margin-top: 17px;
  }

  #dd2 .col1,
  #dd5 .col1,
  #dd3 .col1,
  #dd4 .col1 {
    grid-template-columns: 1fr;
    gap: 34px;
  }

  #dd2 .col1 p,
  #dd5 .col1 p,
  #dd4 .col1 p,
  #dd3 .col1 p {
    display: none;
  }
  #dd2 .col2,
  #dd5 .col2,
  #dd4 .col2,
  #dd3 .col2 {
    margin-top: 17px;
  }

  .btns {
    display: flex;
    flex-direction: column;
    max-width: 348px;
    gap: 10px;
    padding: 15px 24px;
  }
  .btns .btn {
    height: 56px;
  }
}
@media screen and (max-width: 560px) {
  .navbar {
    overflow: hidden;
    max-width: 100%;
    width: fit-content;
    justify-content: flex-start;
    padding: 0;
  }
  .buttons {
    margin-left: auto;
    margin-right: auto;
  }
}
</style>
