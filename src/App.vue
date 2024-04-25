<template>
  <section>
    <nav
      class="header navbar navbar-expand-lg navbar-dark bg-dark border-bottom border-body"
    >
      <div class="container-fluid content">
        <router-link class="navbar-brand" to="/"
          ><img
            class="logo"
            src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b1/Rick_and_Morty.svg/2560px-Rick_and_Morty.svg.png"
            alt=""
            width="300px"
            height="100px"
        /></router-link>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <router-link class="a navbar-brand" to="/Home"
                >Personagens</router-link
              >
            </li>
            <li class="nav-item">
              <router-link class="a navbar-brand" to="/About"
                >Sobre</router-link
              >
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <div class="main">
      <RouterView />
    </div>
  </section>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

section {
  min-height: 100vh;
  background: url("https://m.media-amazon.com/images/S/pv-target-images/3f8ae4a13de932bc679af5272ce983693d773818ff67a774dfcf0592bcd3beb7._SX1080_FMjpg_.jpg")
    no-repeat;
  background-size: cover;
  background-position: center;
}

.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding: 10px;
  background: transparent;
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 100;
}

.logo {
  font-size: 30px;
  color: #fff;
  text-decoration: none;
  font-weight: 700;
}

.nav-item .a {
  position: relative;
  font-size: 18px;
  color: #fff;
  font-weight: 500;
  text-decoration: none;
  margin-left: 40px;
}

.nav-item .a::before {
  content: "";
  position: absolute;
  top: 100%;
  left: 0;
  width: 0;
  height: 2px;
  background: #fff;
  transition: 0.3s;
}

.nav-item .a:hover::before {
  width: 100%;
}

/*







/* 

 */
</style>
