<template>
  <div class="main">
    <div class="welcome">
      <h1 class="title">Bem-vindo de volta!</h1>
      <p class="description">
        Insira seus dados nos campos e conecte-se para aproveitar o máximo das
        funcionalidades do nosso software
      </p>
      <a class="btn-access" href="#">ACESSAR</a>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.main {
  width: 40vw;
  height: 100vh;
  background-image: linear-gradient(#188c6f, #3ab395, #4cb7a8);
  color: #fff;
  text-align: center;
  align-items: center;
  display: flex;
  justify-content: center;
}
.welcome {
  width: 80%;
  margin: 0 auto;
}
.title {
  font-family: InfraBold;
}
.description {
  font-size: 17px;
  padding-bottom: 45px;
  padding-top: 30px;
}
.btn-access {
  background-color: transparent;
  border: 1px solid #fff;
  color: #fff;
  font-size: 17px;
  padding: 15px 70px;
  border-radius: 50px;
  text-decoration: none;
}
.btn-access:hover {
  background-color: #188c6f;
}
</style>
