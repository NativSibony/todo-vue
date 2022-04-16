<template>
  <div class="home">
    <div class="sidebar">
      <app-sidebar></app-sidebar>
    </div>
    <main>
      <app-header></app-header>
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
  font-family: "Poppins", sans-serif;
  font-size: 1.45rem;
  overflow-x: hidden;
  --scrollbarBG: #f0dedb;
  --thumbBG: #f7c8c3;
}

body {
  width: 100vw;
  height: 100vh;
}

.home {
  width: 100%;
  display: grid;
  grid-template-columns: 5% 95%;
}

main {
  padding: 40px;
}

::-webkit-scrollbar {
  width: 11px;
  scrollbar-width: thin;
  scrollbar-color: var(--thumbBG) var(--scrollbarBG);
}

::-webkit-scrollbar-track {
  background: var(--scrollbarBG);
}
::-webkit-scrollbar-thumb {
  background-color: var(--thumbBG);
  border-radius: 6px;
  border: 3px solid var(--scrollbarBG);
}
</style>
