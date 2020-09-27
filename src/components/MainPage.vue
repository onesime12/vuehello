<template>
  <div class="container">
    <div class="centerDiv">
      <h3 class="title">Kilaka-online</h3>
      <h6>{{message}}</h6>
      <input v-model="email" type="text" class="email" placeholder="Email@example.com" /><br />
      <input v-model="password" type="password"  class="password" placeholder="*****" /><br />
      <button @click="connexion" type="button" class="btn-con">Connexion</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainPage",
  data() {
    return {
      email: "",
      password: "",
      message: "",
    };
  },
  methods: {
    connexion() {
      if (this.email === "onesime@app.com" && "123456" === this.password) {
        this.message = "Vous etes connecter";
        this.email=""
        this.password=""
      } else {
        this.message = "conard!!!";
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  width: 600px;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 16px;
  margin: 0 auto;
  height: 400px;
  background-color: #21ce99;
  border-radius: 10px;
}

.title {
  color: white;
  font-size: 40px;
  font-weight: 300;
}
.email {
  padding: 10px;
  margin-bottom: 12px;
  border-radius: 6px;
  border: none;

}
.email:focus{
  border: none;
}
.password {
  padding: 10px;
  margin-bottom: 12px;
  border-radius: 6px;
  border: none;
}
.password:focus{
  border: none;
}
.btn-con {
  margin-top: 20px;
  padding: 10px 40px;
  color: white;
  background-color: black;
  border-radius: 8px;
  border: none;
  cursor: pointer;
}
</style>
