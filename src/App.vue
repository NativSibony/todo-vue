<template>
  <div class="home">
    <div class="sidebar">
      <app-sidebar></app-sidebar>
    </div>
    <main>
      <app-header> </app-header>
      <app-content></app-content>
    </main>
  </div>
</template>

<script>
import Content from "./components/Shared/Content.vue";
import Header from "./components/Shared/Header/Header.vue";
import Sidebar from "./components/Sidebar/Sidebar.vue";

export default {
  components: {
    "app-header": Header,
    "app-content": Content,
    "app-sidebar": Sidebar
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700&display=swap");

*,
*::before,
*::after {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

html {
  background-color: #ece4e3;
  width: 100vw;
  height: 100vh;
  font-family: "Poppins", sans-serif;
  font-size: 1.45rem;
  overflow-x: hidden;
}

.home {
  widows: 100%;
  display: grid;
  grid-template-columns: 5% 95%;
}

main {
  padding: 40px;
}
</style>
