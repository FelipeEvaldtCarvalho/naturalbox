<template>
  <div class="svg-container">
    <svg class="back" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 200">
      <path
        fill="#4C884B"
        fill-opacity="1"
        d="M0,32L30,58.7C60,85,120,139,180,133.3C240,128,300,64,360,74.7C420,85,480,171,540,208C600,245,660,235,720,197.3C780,160,840,96,900,90.7C960,85,1020,139,1080,138.7C1140,139,1200,85,1260,74.7C1320,64,1380,96,1410,112L1440,128L1440,320L1410,320C1380,320,1320,320,1260,320C1200,320,1140,320,1080,320C1020,320,960,320,900,320C840,320,780,320,720,320C660,320,600,320,540,320C480,320,420,320,360,320C300,320,240,320,180,320C120,320,60,320,30,320L0,320Z"
      ></path>
    </svg>
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 200">
      <path
        fill="#B0C372"
        fill-opacity="1"
        d="M0,160L30,165.3C60,171,120,181,180,176C240,171,300,149,360,117.3C420,85,480,43,540,53.3C600,64,660,128,720,133.3C780,139,840,85,900,80C960,75,1020,117,1080,149.3C1140,181,1200,203,1260,192C1320,181,1380,139,1410,117.3L1440,96L1440,320L1410,320C1380,320,1320,320,1260,320C1200,320,1140,320,1080,320C1020,320,960,320,900,320C840,320,780,320,720,320C660,320,600,320,540,320C480,320,420,320,360,320C300,320,240,320,180,320C120,320,60,320,30,320L0,320Z"
      ></path>
    </svg>
  </div>
  <section>
    <h1 class="title">Depoimentos dos clientes</h1>
    <div class="card-container">
      <div class="card" v-for="(card, index) in cards" :key="index">
        <div>
          <img :src="card.img" :alt="card.name" />
          <h2>{{ card.name }}</h2>
        </div>
        <p>{{ `"${card.coment}"` }}</p>
        <span class="stars"
          ><ion-icon v-for="n in 5" :key="n" name="star"></ion-icon
        ></span>
      </div>
    </div>
  </section>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 200">
    <path
      fill="#B0C372"
      fill-opacity="1"
      d="M0,0L120,42.7C240,85,480,171,720,181.3C960,192,1200,128,1320,96L1440,64L1440,0L1320,0C1200,0,960,0,720,0C480,0,240,0,120,0L0,0Z"
    ></path>
  </svg>
</template>

<script>
export default {
  name: "NbFeedBacks",
  data() {
    return {
      cards: [
        {
          img: require("@/assets/profile1.png"),
          name: "Carlos Montana",
          coment:
            "Sou cliente há anos, e nunca cogitei trocar de fornecedor de orgânicos. Os produtos são ótimos, e a qualidade do serviço é perfeita.",
        },
        {
          img: require("@/assets/profile2.png"),
          name: "Camila Miranda",
          coment:
            "Produtos sempre fresquinhos toda a semana em casa. Não preciso me preocupar indo em supermercados ou feiras. Faça chuva ou faça sol temos nossa entrega garantida. Obrigada!",
        },
        {
          img: require("@/assets/profile3.png"),
          name: "Clóvis Machado",
          coment:
            "Amo a Natural Box! Facilita o meu dia a dia recebendo a feira toda semana na porta de casa com produtos fresquinhos e sem agrotóxicos.",
        },
      ],
    };
  },
};
</script>

<style scoped>
section {
  background-color: #b0c372;
  padding: 0 5vw;
  padding-bottom: 10vw;
}
.title {
  text-align: center;
  font-family: "Amatic SC", cursive;
  font-size: 4.4vw;
}
.svg-container {
  position: relative;
  height: 13.45vw;
}
.back {
  position: absolute;
  top: 0;
  z-index: -1;
}
.card-container {
  margin-top: 4vw;
  display: flex;
  width: 100%;
  gap: 3.3vw;
  justify-content: space-evenly;
}
.card {
  width: 25vw;
  border-radius: 1.1vw;
  display: flex;
  flex-direction: column;
  gap: 2vw;
  background-color: #f2ebd1;
  text-align: center;
  padding: 2vw;
  transition: all 0.5s ease;
  justify-content: space-between;
}
.card:hover {
  transform: scale(1.05);
}
.card img {
  border-radius: 50%;
  width: 10vw;
  align-self: center;
  border: 0.2vw solid #2d2d2d;
}
.card h2 {
  font-size: 2.2vw;
}
.card p {
  font-size: 1.6vw;
}
.stars {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1.1vw;
}
.stars ion-icon {
  font-size: 2vw;
  color: #ed7d2b;
}
@media screen and (max-width: 735px) {
  section {
    padding: 15vw 9vw;
    padding-bottom: 20vw;
  }
  .title {
    font-size: 10vw;
  }

  .card-container {
    margin-top: 10vw;
    flex-direction: column;
    gap: 10vw;
  }
  .card {
    width: 100%;
    border-radius: 2.1vw;
    gap: 4vw;
    padding: 4vw 6vw;
  }
  .card img {
    width: 35vw;
    border: 0.7vw solid #2d2d2d;
  }
  .card h2 {
    font-size: 5.5vw;
  }
  .card p {
    font-size: 4.6vw;
  }
  .stars {
    gap: 2.1vw;
  }
  .stars ion-icon {
    font-size: 5vw;
    color: #ed7d2b;
  }
}
</style>
