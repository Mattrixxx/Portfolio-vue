<template>
  <div class="homepage">
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
</style>
