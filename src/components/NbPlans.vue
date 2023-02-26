<template>
  <section>
    <h1 class="title">quanto custa?</h1>
    <div class="card-container">
      <div class="card" v-for="(card, index) in cards" :key="index">
        <div class="card-title">
          <h2>Natural Box</h2>
          <h2>{{ card.size }}</h2>
        </div>
        <div class="card-price">
          <h1>R$ {{ card.price }},00</h1>
          <h2>POR MÊS</h2>
        </div>
        <h3>
          <span class="contrast">{{ card.productsNumber }} hortifrutis</span> a
          cada semana para compor o seu kit. Ideal para até
          <span class="contrast">{{ card.peopleNumber }} pessoas.</span>
        </h3>
        <p>É entregue 4 kits por mês. Frete incluso no valor da mensalidade.</p>
        <nb-button :fullWidth="true">Assinar</nb-button>
      </div>
    </div>
  </section>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 120">
    <path
      fill="#F2D799"
      fill-opacity="1"
      d="M0,64L80,80C160,96,320,128,480,117.3C640,107,800,53,960,32C1120,11,1280,21,1360,26.7L1440,32L1440,0L1360,0C1280,0,1120,0,960,0C800,0,640,0,480,0C320,0,160,0,80,0L0,0Z"
    ></path>
  </svg>
</template>

<script>
import NbButton from "./NbButton.vue";
export default {
  components: { NbButton },
  name: "NbPlans",
  data() {
    return {
      cards: [
        {
          size: "Pequeno",
          price: 255,
          productsNumber: 6,
          peopleNumber: 2,
        },
        {
          size: "Médio",
          price: 295,
          productsNumber: 8,
          peopleNumber: 4,
        },
        {
          size: "Grande",
          price: 390,
          productsNumber: 12,
          peopleNumber: 6,
        },
      ],
    };
  },
};
</script>

<style scoped>
section {
  background-color: #f2d799;
  padding: 5vw;
}
.title {
  text-align: center;
  font-family: "Amatic SC", cursive;
  font-size: 4.4vw;
}
.card-container {
  margin-top: 4vw;
  display: flex;
  width: 100%;
  gap: 3.3vw;
  justify-content: space-between;
}
.card {
  border-radius: 2.2vw;
  display: flex;
  flex-direction: column;
  gap: 2vw;
  background-color: #f2ebd1;
  text-align: center;
  padding: 4vw;
  transition: all 0.5s ease;
}
.card:hover {
  transform: scale(1.03);
}
.card-title h2 {
  font-size: 2.2vw;
  font-weight: 700;
}
.card-price h1 {
  color: #4b884a;
  font-size: 2.6vw;
  font-weight: 700;
}
.card-price h2 {
  color: #4b884a;
  font-size: 2vw;
  font-weight: 400;
}
.card h3 {
  font-size: 1.5vw;
}
.card p {
  font-size: 1.2vw;
}
@media screen and (max-width: 735px) {
  section {
    padding: 15vw 5vw;
  }
  .title {
    text-align: center;
    font-family: "Amatic SC", cursive;
    font-size: 10vw;
  }
  .card-container {
    flex-direction: column;
    gap: 15vw;
    padding: 10vw;
  }

  .card {
    gap: 6vw;
    padding: 6vw;
  }
  .card-title h2 {
    font-size: 6vw;
  }
  .card-price h1 {
    font-size: 7.5vw;
  }
  .card-price h2 {
    font-size: 4.5vw;
  }
  .card h3 {
    font-size: 4.5vw;
  }
  .card p {
    font-size: 3.5vw;
  }
}
</style>
