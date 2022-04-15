<template>
  <div class="header">
    <app-search-bar></app-search-bar>
    <app-add-task></app-add-task>
  </div>
</template>

<script>
import AddTask from "./AddTask.vue";
import SearchBar from "./SearchBar.vue";
export default {
  components: {
    "app-search-bar": SearchBar,
    "app-add-task": AddTask
  }
};
</script>

<style>
.header {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  row-gap: 20px;
}
</style>
