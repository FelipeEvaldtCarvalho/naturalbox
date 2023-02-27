<template>
  <footer>
    <div class="left-content">
      <h1 class="title">NaturalBox</h1>
      <p>Inscreva-se para se manter informado!</p>
      <input type="email" placeholder="E-mail" />
      <nb-button> Inscreva-se</nb-button>
      <p>
        Ao inscrever-se, você aceita os <a href="">Termos de Uso</a> e
        <a href="">Politica de Privacidade</a>.
      </p>
    </div>
    <div class="right-content">
      <span class="social">
        <ion-icon class="logo-instagram" name="logo-instagram"></ion-icon>
        <ion-icon class="logo-facebook" name="logo-facebook"></ion-icon>
        <ion-icon class="logo-youtube" name="logo-youtube"></ion-icon>
        <ion-icon class="logo-whatsapp" name="logo-whatsapp"></ion-icon>
      </span>
      <div>
        <p>Copyright © 2023 Natural Box.</p>
        <p>
          Desenvolvido por
          <a href="https://felipecarvalho.tech/">Felipe Carvalho.</a>
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
import NbButton from "./NbButton.vue";
export default {
  components: { NbButton },
  name: "NbFooter",
};
</script>

<style scoped>
footer {
  background-color: #f2ebd1;
  position: relative;
  padding: 5vw;
  display: flex;
  width: 100%;
}
.title {
  text-align: center;
  font-family: "Amatic SC", cursive;
  font-size: 5.5vw;
}
.left-content {
  display: flex;
  flex-direction: column;
  gap: 3.3vw;
  width: 50%;
  padding: 0 7vw;
}
.left-content p {
  font-size: 1.8vw;
}
.left-content a {
  color: #9a4725;
  font-weight: 700;
}
.left-content input {
  border-radius: 0.3vw;
  border: none;
  font-size: 1.4vw;
  font-weight: 400;
  padding: 1.1vw 1.1vw;
  transition: all 0.5s ease;
}
.left-content input:focus {
  outline: none;
}
.right-content {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  gap: 3.3vw;
  width: 50%;
  padding: 0 7vw;
}
.social {
  margin-top: 2.2vw;
  font-size: 3.3vw;
  display: flex;
  justify-content: center;
  gap: 2.2vw;
}
.social ion-icon {
  transition: all 0.5s ease;
  cursor: pointer;
}
.social ion-icon:hover {
  transform: scale(1.2);
}
.logo-instagram {
  color: #4c884b;
}
.logo-facebook {
  color: #ed7d2b;
}
.logo-youtube {
  color: #f1c34a;
}
.logo-whatsapp {
  color: #9a4725;
}
.right-content p {
  text-align: center;
  font-size: 1.8vw;
}
.right-content a {
  color: #9a4725;
  font-weight: 400;
  text-decoration: none;
}
@media screen and (max-width: 735px) {
  footer {
    flex-direction: column;
    padding: 15vw 9vw;
  }
  .title {
    font-size: 13vw;
  }
  .left-content {
    gap: 6vw;
    width: 100%;
    padding: 0 0;
  }
  .left-content p {
    font-size: 4.6vw;
  }
  .left-content a {
    color: #9a4725;
    font-weight: 700;
  }
  .left-content input {
    border-radius: 1.2vw;
    font-size: 4.4vw;
    padding: 3.3vw 3.3vw;
  }
  .right-content {
    gap: 8vw;
    width: 100%;
    padding: 12vw 0;
    padding-bottom: 0;
  }
  .social {
    font-size: 8vw;
    display: flex;
    justify-content: center;
    gap: 9vw;
    transition: all 0.5s ease;
  }

  .right-content p {
    text-align: center;
    font-size: 4.6vw;
  }
}
</style>
