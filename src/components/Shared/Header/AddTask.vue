<template>
  <div>
    <div class="options">
      <v-icon name="bars"></v-icon>
      <v-icon name="th-large" style="fill:#f08a47"></v-icon>
    </div>
    <button>Add Task</button>
  </div>
</template>

<script>
import Icon from "vue-awesome/components/Icon";
import "vue-awesome/icons/bars";
import "vue-awesome/icons/th-large";

export default {
  components: {
    "v-icon": Icon
  }
};
</script>

<style scoped>
.options {
  display: flex;
  flex-direction: row;
  column-gap: 10px;
}

.active {
  fill: #f08a47;
}

.options svg {
  fill: #999;
  width: 19px;
  height: 19px;
}

div {
  display: flex;
  justify-content: space-between;
  padding: 5px;
}
button {
  padding: 8px 10px;
  border: none;
  border-radius: 10px;
  background-color: #f08a47;
  font-family: "Poppins", sans-serif;
  color: white;
  font-size: 0.7rem;
  cursor: pointer;
  transition: 0.2s;
}
button:hover {
  background-color: #fff;
  color: #f08a47;
}
</style>
