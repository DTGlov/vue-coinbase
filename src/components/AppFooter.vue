<template>
  <footer>
    <div class="footer-container">
      <div class="left">
        <div>
          <img src="../assets/coinlogo.svg" alt="" />
        </div>
        <select name="" id="">
          <option value="">English</option>
        </select>
        <p class="base">© 2021 Coinbase</p>
        <p class="socials">Blog • Twitter • Facebook</p>
      </div>
      <div class="links">
        <ul>
          <h2>Company</h2>
          <li>About</li>
          <li>Careers</li>
          <li>Affiliates</li>
          <li>Blog</li>
          <li>Press</li>
          <li>Investors</li>
          <li>Legal & privacy</li>
          <li>Cookie policy</li>
          <li>Cookie preferences</li>
        </ul>
        <ul>
          <h2>Individuals</h2>
          <li>Buy & sell</li>
          <li>Earn free crypto</li>
          <li>Wallet</li>
          <li>Card</li>
          <li>Prime</li>
          <li>Commerce</li>
          <li>Asset Hub</li>
          <li>Custody</li>
        </ul>
        <ul>
          <h2>Support</h2>
          <li>Help center</li>
          <li>Contact us</li>
          <li>Create account</li>
          <li>ID verification</li>
          <li>Account information</li>
          <li>Payment methods</li>
          <li>Account access</li>
          <li>Supported crypto</li>
          <li>Supported countries</li>
          <li>Status</li>
        </ul>
        <ul>
          <h2>Learn</h2>
          <li>Crypto basics</li>
          <li>Tips & tutorials</li>
          <li>Market updates</li>
          <li>What is Bitcoin?</li>
          <li>What is crypto?</li>
          <li>What is a blockchain?</li>
          <li>How to set up a crypto wallet</li>
          <li>How to send crypto</li>
          <li>Taxes</li>
        </ul>
        <ul>
          <h2>Developers</h2>
          <li>Coinbase Cloud</li>
          <li>Connect</li>
          <li>Pro</li>
          <li>Bison Trails</li>
          <li>WalletLink</li>
          <li>Rosetta</li>
          <li>USDC</li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
};
</script>

<style scoped>
footer {
  padding-top: 100px;
  padding-bottom: 100px;
}
.footer-container {
  display: flex;
  width: 85%;
  margin: 0 auto;
  flex-direction: column;
}
.left {
  /* width: 40%; */
  opacity: 0.7;
  font-size: 18px;
  color: rgb(17, 51, 85);
}
select {
  font-family: inherit;
  width: 270px;
  height: 30px;
  font-size: 16px;
  font-weight: 500;
  margin-top: 20px;
}
img {
  width: 50%;
}
.base {
  margin-top: 15px;
}
.socials {
  margin-top: 5px;
}
p {
  /* margin-top: 15px; */
}
.links {
  display: flex;
  width: 60%;
  flex-wrap: wrap;
  flex-direction: column;
  margin-top: 20px;
}
ul {
  /* width: 30%; */
}
li {
  list-style-type: none;
  font-size: 18px;
  line-height: 1.3;
  opacity: 0.7;
  color: rgb(17, 51, 85);
  text-decoration: none;
  max-width: 200px;
  margin-bottom: 10px;
}
h2 {
  margin-bottom: 12px;
  margin-top: 10px;
  font-size: 16px;
  font-weight: 800;
  color: rgb(17, 51, 85);
  font-size: 18px;
}
@media only screen and (min-width: 992px) {
  footer {
    padding-top: 100px;
    padding-bottom: 100px;
  }
  .footer-container {
    flex-direction: row;
    width: 85%;
    margin: 0 auto;
  }
  .left {
    width: 40%;
    opacity: 0.7;
    color: rgb(17, 51, 85);
  }
  select {
    font-family: inherit;
    width: 250px;
    height: 30px;
    font-size: 16px;
    font-weight: 500;
    margin-top: 20px;
  }
  img {
    width: 30%;
  }
  p {
    /* margin-top: 15px; */
  }
  .links {
    flex-direction: row;
    width: 60%;
    flex-wrap: wrap;
    margin-top: 0;
  }
  ul {
    width: 30%;
  }
  li {
    list-style-type: none;
    font-size: 16px;
    line-height: 1.3;
    opacity: 0.7;
    color: rgb(17, 51, 85);
    text-decoration: none;
    max-width: 200px;
    margin-bottom: 10px;
  }
  h2 {
    margin-bottom: 12px;
    margin-top: 0px;
    font-size: 16px;
    font-weight: 800;
    color: rgb(17, 51, 85);
    font-size: 18px;
  }
}
</style>