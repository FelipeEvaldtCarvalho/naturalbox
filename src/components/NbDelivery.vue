<template>
  <section>
    <div class="container">
      <div class="text-content">
        <h1 class="title">quando é feita a entrega?</h1>
        <p>
          A assinatura funciona para toda região metropolitana de Porto Alegre,
          Rio Grande do Sul.
        </p>
        <div class="card" v-for="(card, index) in cards" :key="index">
          <ion-icon name="calendar-outline"></ion-icon>
          <div class="card-text">
            <h2>{{ card.weekDay }}</h2>
            <h3>Das {{ card.startTime }} às {{ card.endTime }}</h3>
          </div>
        </div>
      </div>
      <div class="img-content">
        <img src="../assets/bag.png" alt="" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "NbDelivery",
  data() {
    return {
      cards: [
        {
          weekDay: "Segunda-Feira",
          startTime: "09h00",
          endTime: "14h00",
        },
        {
          weekDay: "Quarta-Feira",
          startTime: "15h30",
          endTime: "20h00",
        },
        {
          weekDay: "Sexta-Feira",
          startTime: "10h30",
          endTime: "15h30",
        },
        {
          weekDay: "Sábado",
          startTime: "11h00",
          endTime: "15h00",
        },
      ],
    };
  },
};
</script>

<style scoped>
section {
  padding: 5vw;
}
.title {
  text-align: center;
  font-family: "Amatic SC", cursive;
  font-size: 4.4vw;
}
.container {
  display: flex;
  width: 100%;
}
.text-content {
  display: flex;
  flex-direction: column;
  width: 50%;
  gap: 3.3vw;
}
.text-content p {
  text-align: center;
  font-size: 2vw;
  font-weight: 400;
}
.text-content ion-icon {
  font-size: 4vw;
  color: #4b884a;
}
.img-content {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 50%;
}
.img-content img {
  height: 45vw;
}
.card {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1.1vw;
}
.card-text h2 {
  font-size: 2.2vw;
  font-weight: 700;
}
.card-text h3 {
  font-size: 2.2vw;
  font-weight: 400;
}
@media screen and (max-width: 735px) {
  section {
    padding: 15vw 9vw;
  }
  .title {
    font-size: 10vw;
  }
  .container {
    flex-direction: column;
    position: relative;
  }
  .text-content {
    width: 100%;
    gap: 6vw;
  }
  .text-content p {
    font-size: 4.2vw;
  }
  .text-content ion-icon {
    font-size: 8vw;
  }
  .img-content {
    bottom: 0;
    right: 0;
    justify-content: end;
    z-index: -1;
    position: absolute;
    width: 100%;
  }
  .img-content img {
    height: 90vw;
    opacity: 0.2;
  }
  .card {
    gap: 3.3vw;
  }
  .card-text h2 {
    font-size: 4.4vw;
  }
  .card-text h3 {
    font-size: 4.4vw;
  }
}
</style>
