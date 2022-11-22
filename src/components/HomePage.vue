<template>
  <div class="homepage">
    <!-- Nav Section -->
    <nav>
      <div class="container">
        <div class="nav-con">
          <div class="logo">
            <h3>Portfo<span>lio</span></h3>
          </div>
          <ul class="menu" id="sidemenu">
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Blog</a></li>
            <li><a href="#">Service</a></li>
            <li><a href="#">Contact Us</a></li>
            <font-awesome-icon icon="fa-solid fa-xmark" @click="closemenu()" />
          </ul>
          <font-awesome-icon icon="fa-solid fa-bars" @click="openmenu()" />
        </div>
      </div>
    </nav>

    <!-- Home Section -->

    <div class="home">
      <div class="container">
        <div class="text-home">
          <h4>Hello, My name is</h4>
          <h1>I'm Thanundorn<span> (Ming)</span></h1>
          <h3>I'm a Web Developer.</h3>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    openmenu() {
      const sidemenu = document.getElementById("sidemenu");
      sidemenu.style.right = "0";
    },
    closemenu() {
      const sidemenu = document.getElementById("sidemenu");
      sidemenu.style.right = "-200px";
    },
  },
  mounted() {},
};
</script>

<style scoped>
.homepage {
}
.container {
  max-width: 1170px;
  margin: 0 auto;
  padding: 0px 5%;
}

/* Nav Section */
nav {
  background-color: var(--black);
  color: var(--white);
  height: 80px;
}
nav .svg-inline--fa {
  display: none;
}
.nav-con {
  display: flex;
  justify-content: space-between;
  height: 80px;
  align-items: center;
}
.logo h3 {
  font-size: 1.75rem;
  color: var(--yellow);
}
.logo h3 span {
  color: var(--white);
}
ul.menu li {
  display: inline-block;
  list-style: none;
  margin: 0 1rem;
}
ul.menu li a {
  color: var(--white);
  font-weight: 600;
  text-decoration: none;
  position: relative;
}
ul.menu li a::after {
  content: "";
  width: 0;
  height: 3px;
  background: var(--yellow);
  position: absolute;
  left: 0;
  bottom: -6px;
  transition: 0.5s;
}
ul.menu li a:hover::after {
  width: 100%;
}

/* Mobile Nav */
@media only screen and (max-width: 600px) {
  nav .svg-inline--fa {
    display: block;
    font-size: 25px;
  }
  ul.menu {
    background-color: var(--yellow);
    position: fixed;
    top: 0;
    right: -200px;
    width: 200px;
    height: 100vh;
    padding-top: 50px;
    z-index: 2;
    transition: right 0.5s;
  }
  ul.menu li {
    display: block;
    margin: 25px;
  }
  ul.menu .svg-inline--fa {
    position: absolute;
    top: 25px;
    left: 25px;
    cursor: pointer;
  }
}

/* Home Section*/
.home {
  width: 100%;
  height: 85vh;
  background-image: url(../assets/bg.png);
  background-size: cover;
  background-position: center;
}
.text-home {
  position: absolute;
  top: 40%;
}
.text-home h1 {
  color: var(--white);
  font-size: 50px;
}
.text-home h3 {
  color: var(--white);
  font-size: 25px;
}
.text-home h4 {
  color: var(--white);
  font-size: 20px;
}
.text-home span {
  color: var(--yellow);
}
/* Mobile Home */
@media only screen and (max-width: 1400px) {
  .home {
    height: 50vh;
  }
  .text-home {
    top: 25%;
  }
}
@media only screen and (max-width: 990px) {
  .text-home h1 {
    font-size: 40px;
  }
}
@media only screen and (max-width: 900px) {
  .home {
    height: 36vh;
  }
  .text-home {
    top: 20%;
  }
}
@media only screen and (max-width: 800px) {
  .text-home h1 {
    font-size: 30px;
  }
  .text-home h3 {
    font-size: 20px;
  }
  .text-home h4 {
    font-size: 15px;
  }
}
@media only screen and (max-width: 600px) {
  .home {
    background-image: url(../assets/bg1.png);
    height: 100vh;
  }
  .text-home {
    top: 30%;
  }
  .text-home h1 {
    font-size: 40px;
  }
  .text-home h3 {
    font-size: 25px;
  }
  .text-home h4 {
    font-size: 20px;
  }
}
</style>
