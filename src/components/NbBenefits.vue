<template>
  <section>
    <h1 class="title">Benefícios</h1>
    <div class="card-container">
      <div class="card" v-for="(card, index) in cards" :key="index">
        <div class="card-header">
          <img :src="card.img" :alt="card.title" />
          <h1>{{ card.title }}</h1>
        </div>
        <p>{{ card.description }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "NbBenefits",
  data() {
    return {
      cards: [
        {
          title: "Economia",
          description:
            "Mais barato que o mercado. Direto na porta da sua casa, sem precisar sair para fazer compras.",
          img: require("@/assets/coin.png"),
        },
        {
          title: "Qualidade",
          description:
            "Produtos da safra, de acordo com a estação. Isso garante maior variedade. Diversificando os orgânicos da sua mesa.",
          img: require("@/assets/apple.png"),
        },
        {
          title: "Faça a Diferença",
          description:
            "Você incentiva o pequeno produtor, respeita a natureza e não prejudica a sua saúde.",
          img: require("@/assets/like.png"),
        },
      ],
    };
  },
};
</script>

<style scoped>
.title {
  text-align: center;
  font-family: "Amatic SC", cursive;
  font-size: 4.4vw;
}
.card-container {
  display: flex;
  width: 100%;
  padding: 3.3vw;
  justify-content: space-around;
  margin-bottom: 7vw;
}
.card {
  display: flex;
  flex-direction: column;
  width: 23vw;
  gap: 3.3vw;
}
.card-header {
  display: flex;
  align-items: center;
  gap: 1.1vw;
}
.card-header img {
  height: 5.2vw;
}
.card-header h1 {
  font-size: 2.2vw;
  font-weight: 700;
}
.card p {
  font-size: 2vw;
  text-align: center;
}
@media screen and (max-width: 735px) {
  .title {
    text-align: center;
    font-family: "Amatic SC", cursive;
    font-size: 10vw;
  }
  .card-container {
    flex-direction: column;
    padding: 10vw;
  }
  .card {
    width: 100%;
    align-items: center;
    margin-bottom: 12vw;
  }
  .card-header img {
    height: 7vw;
  }
  .card-header h1 {
    font-size: 6vw;
  }
  .card p {
    font-size: 4.5vw;
  }
}
</style>
