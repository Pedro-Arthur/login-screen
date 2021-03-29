<template>
  <div class="main">
    <div class="login">
      <h2 class="title">Entre e saiba mais!</h2>

      <div class="buttons">
        <a href="#" class="button-facebook">
          <i class="fa fa-facebook"></i>
        </a>
        <a href="#" class="button">
          <i class="fa fa-google"></i>
        </a>
        <a href="#" class="button">
          <i class="fa fa-linkedin"></i>
        </a>
      </div>

      <p class="subtitle">Ou use sua conta do email para efetuar o login</p>

      <div class="input-box">
        <div class="icon">
          <i class="fa fa-envelope"></i>
        </div>
        <input type="email" class="input" placeholder="Email" />
      </div>

      <div class="input-box">
        <div class="icon">
          <i class="fa fa-lock"></i>
        </div>
        <input :type="input_type" class="input" placeholder="Senha" />
        <div class="icon">
          <a class="hidden-pass" v-on:click="password_control" href="#"><i :class="icon_pass"></i></a>
        </div>
      </div>

      <div class="forgot">
        <a href="#" class="forgot-password">Esqueceu sua senha?</a>
      </div>

      <a href="#" class="btn-login">LOGIN</a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input_type: "password",
      icon_pass: "fa fa-eye",
    };
  },

  computed: {
    isPassword() {
      return this.input_type === "password", this.icon_pass === "fa fa-eye";
    },
  },

  methods: {
    password_control() {
      this.input_type = this.isPassword ? "text" : "password";
      this.icon_pass = this.isPassword ? "fa fa-eye-slash" : "fa fa-eye";
    },
  },
};
</script>

<style scoped>
.main {
  width: 60vw;
  height: 100vh;
  align-items: center;
  display: flex;
  justify-content: center;
  text-align: center;
}
.title {
  color: #3ab395;
  margin-bottom: 30px;
  text-align: center;
  font-family: InfraBold;
}
.subtitle {
  text-align: center;
  color: #808080;
  margin-top: 30px;
  padding: 0 30px;
}
.buttons {
  display: flex;
  width: 70%;
  margin: 0 auto;
  justify-content: space-around;
}
.button {
  padding: 10px 16px;
  border-radius: 100px;
  border: 1px solid #dedede;
  color: #353233;
}
.button-facebook {
  padding: 10px 18px;
  border-radius: 100px;
  border: 0.3px solid #dedede;
  color: #353233;
}
.button:hover {
  background-color: #eee;
}
.button-facebook:hover {
  background-color: #eee;
}
.input-box {
  background-color: #f4f8f7;
  margin: 0 auto;
  margin-top: 10px;
  justify-content: flex-start;
  padding: 12px 17px;
  color: #808080;
  display: flex;
}
.icon {
  width: 7%;
  text-align: center;
}
.input {
  padding-left: 12px;
  background-color: transparent;
  box-shadow: 0 0 0 0;
  border: 0 none;
  outline: 0;
  width: 93%;
  color: #808080;
  font-family: InfraLight;
}
.forgot {
  margin-top: 30px;
  margin-bottom: 50px;
  padding: 10px;
  text-align: center;
}
.forgot-password {
  color: #353233;
  font-size: 18px;
  text-decoration: none;
  border-bottom: 1px solid #dedede;
  padding: 5px;
}
.forgot-password:hover {
  color: #3ab395;
  font-size: 18px;
  text-decoration: none;
  border-bottom: 1px solid #eee;
  padding: 5px;
}
.btn-login {
  background-color: #3ab395;
  color: #fff;
  font-size: 17px;
  padding: 15px 70px;
  border-radius: 50px;
  text-decoration: none;
  margin: 0 auto;
}
.btn-login:hover {
  background-color: #4cb7a8;
}
.hidden-pass {
  text-decoration: none;
  color: #808080;
}
</style>