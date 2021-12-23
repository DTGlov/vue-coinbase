<template>
  <div class="con">
    <header>
      <nav id="nav">
        <router-link class="link" to="/">
          <img src="../assets/coinlogo.svg" alt="coinbase-logo" />
        </router-link>
        <ul class="link-wrapper">
          <li>
            <router-link to="/prices">Prices</router-link>
          </li>
          <li>
            <router-link to="/">Learn</router-link>
          </li>
          <li>
            <router-link to="/">Individuals</router-link>
          </li>
          <li><router-link to="/">Businesses</router-link></li>
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
    <div class="drop-section" v-if="show">
      <div class="drop-container">
        <div class="drop">
          <p>Prices</p>
          <!-- <i class="fas fa-chevron-down"></i> -->
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
    };
  },
  methods: {
    toggleShow() {
      this.show = !this.show;
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
    margin-left: 150px;
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
}
</style>