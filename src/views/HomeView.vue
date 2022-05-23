<template>
  <h1 class="home">Home</h1>
  <div class="link">
    <router-link to="./quiz">Vueクイズへ</router-link>
    <router-link to="./palette">Vueパレットへ</router-link>
    <router-link to="./memo">Vueメモへ</router-link>
  </div>
</template>

<style scoped>
.home {
  width: 95%;
  text-align: center;
  border-bottom: solid 5px #366;
}
.link {
  display: flex;
  flex-direction: column;
  text-align: center;
}
a {
  text-decoration: none;
  color: rgb(74, 178, 143);
  font-size: xx-large;
  font-weight: bolder;
  margin-right: 5%;
}
a:hover {
  text-decoration: underline;
}
</style>
