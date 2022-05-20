<template>
  <h1 class="home">Home</h1>
  <div class="link">
    <a href="./quiz">Vueクイズへ</a>
    <a href="./palette">Vueパレットへ</a>
    <a href="./memo">Vueメモへ</a>
  </div>
</template>

<style>
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
}
a:hover {
  text-decoration: underline;
}
</style>
