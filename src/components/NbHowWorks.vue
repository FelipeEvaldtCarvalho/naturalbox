<template>
  <section>
    <h1 class="title">como funciona?</h1>
    <div class="card-container">
      <div class="card" v-for="(card, index) in cards" :key="index">
        <img :src="card.img" />
        <p>{{ card.text }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "NbHowWorks",
  data() {
    return {
      cards: [
        {
          img: require("@/assets/shop.png"),
          text: "1 - Você assina o plano que mais te agrada",
        },
        {
          img: require("@/assets/separate.png"),
          text: "2 - Semanalmente selecionamos os melhores produtos para você",
        },
        {
          img: require("@/assets/delivery.png"),
          text: "3 - Entregamos para você  gratuitamente",
        },
      ],
    };
  },
};
</script>

<style scoped>
section {
  background-color: #f2ebd1;
  padding: 5vw;
}
.title {
  text-align: center;
  font-family: "Amatic SC", cursive;
  font-size: 4.4vw;
}
.card-container {
  display: flex;
  width: 100%;
  padding: 3.3vw;
  gap: 3.3vw;
  justify-content: space-around;
}
.card {
  width: 30%;
  text-align: center;
}
.card img {
  height: 13vw;
}
.card p {
  margin-top: 3.3vw;
  font-size: 2vw;
  font-weight: 700;
  color: #9a4725;
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
    width: 100%;
  }
  .card img {
    height: 25vw;
  }
  .card p {
    margin-top: 5vw;
    font-size: 5vw;
    font-weight: 700;
    color: #9a4725;
  }
}
</style>
