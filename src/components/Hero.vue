<template>
  <header>
    <nav>
      <h1 class="logo">NaturalBox</h1>
      <div v-if="windowWidth > 735" class="nav-links">
        <a href="#">Planos</a>
        <nb-button>Assinar</nb-button>
      </div>
      <div v-else class="mobile-menu">
        <button
          class="mobile-btn"
          @focus="mobileModal = true"
          @blur="mobileModal = false"
        >
          <ion-icon name="menu-outline"></ion-icon>
        </button>
        <div class="mobile-modal" v-if="mobileModal">
          <a href="#">Planos</a>
          <nb-button>Assinar</nb-button>
        </div>
      </div>
    </nav>
    <div class="container">
      <div class="hero-text">
        <h1>Receba a natureza na sua porta</h1>
        <p>
          Uma alimentação orgânica não é apenas uma questão de
          <span class="contrast">sabor</span> e
          <span class="contrast">qualidade</span>, mas também de cuidado com a
          <span class="contrast">saúde</span> e o
          <span class="contrast">meio ambiente</span>.
        </p>
        <nb-button>Assinar</nb-button>
      </div>
      <div class="hero-img">
        <img src="../assets/header-img.png" alt="" />
      </div>
    </div>
  </header>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 230">
    <path
      fill="#F2EBD1"
      fill-opacity="1"
      d="M0,64L80,85.3C160,107,320,149,480,144C640,139,800,85,960,90.7C1120,96,1280,160,1360,192L1440,224L1440,0L1360,0C1280,0,1120,0,960,0C800,0,640,0,480,0C320,0,160,0,80,0L0,0Z"
    ></path>
  </svg>
</template>

<script>
import NbButton from "./NbButton.vue";
export default {
  components: { NbButton },
  name: "HeroBanner",
  data() {
    return {
      windowWidth: null,
      mobileModal: false,
    };
  },
  mounted() {
    this.windowWidth = window.innerWidth;
    window.addEventListener("resize", () => {
      this.windowWidth = window.innerWidth;
    });
  },
};
</script>

<style scoped lag="sass">
header {
  background-color: #f2ebd1;
}
nav {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: space-between;
  background-color: #f2ebd1;
  padding: 2.2vw 4.4vw;
}
.logo {
  font-family: "Amatic SC", cursive;
  font-size: 4.4vw;
}
a {
  font-size: 1.2rem;
  font-weight: 700;
  text-decoration: none;
  padding: 0.7rem 0;
}
.nav-links {
  display: flex;
  align-items: center;
  gap: 6rem;
}
.container {
  display: flex;
  width: 100%;
  padding: 2rem;
  padding-bottom: 0;
}
.hero-text {
  width: 50%;
  padding: 2.1vw;
  padding-bottom: 0;
  display: flex;
  flex-direction: column;
  gap: 3.3vw;
}
.hero-text h1 {
  font-size: 4.8vw;
  font-weight: 700;
  text-align: left;
}
.hero-text p {
  font-size: 2.1vw;
  font-weight: 400;
  text-align: left;
}
.hero-text button {
  align-self: center;
}
.hero-img {
  width: 50%;
  padding: 2rem;
  padding-bottom: 0;
  display: flex;
  align-items: center;
  justify-content: center;
}
.hero-img img {
  width: 100%;
}
.mobile-menu {
  position: relative;
}
.mobile-menu .mobile-modal {
  -webkit-box-shadow: 0px 0px 15px -1px rgba(0, 0, 0, 0.75);
  -moz-box-shadow: 0px 0px 15px -1px rgba(0, 0, 0, 0.75);
  box-shadow: 0px 0px 15px -1px rgba(0, 0, 0, 0.75);
  background-color: #f2ebd1;
  border-radius: 0.5rem;
  padding: 1rem;
  position: absolute;
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 1rem;
  right: 0;
}
.mobile-menu .mobile-btn {
  display: flex;
  align-self: center;
  font-size: 10vw;
  border: none;
  background-color: transparent;
}
@media screen and (max-width: 735px) {
  nav {
    padding: 4vw 8vw;
  }
  .container {
    display: flex;
    flex-direction: column-reverse;
  }
  .hero-text {
    width: 100%;
    gap: 8.5vw;
  }
  .hero-text h1 {
    font-size: 8.5vw;
  }
  .hero-text p {
    font-size: 5vw;
  }
  .hero-img {
    width: 100%;
    padding: 2.2vw;
  }
  .hero-img img {
    width: 100%;
  }
  .logo {
    font-family: "Amatic SC", cursive;
    font-size: 12vw;
  }
}
</style>
