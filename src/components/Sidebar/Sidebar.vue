<template>
  <div class="side">
    <img src="../../assets/logo.png" alt="logo" />
    <v-icon v-for="icon in icons" :name="icon" :key="icon"></v-icon>
  </div>
</template>

<script>
import Icon from "vue-awesome/components/Icon";
import "vue-awesome/icons/list-alt";
import "vue-awesome/icons/calendar-check";
import "vue-awesome/icons/cog";
export default {
  data() {
    return {
      icons: ["list-alt", "calendar-check", "cog"]
    };
  },
  components: {
    "v-icon": Icon
  }
};
</script>

<style scoped>
.side {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #fff;
  row-gap: 30px;
  padding: 20px;
  height: 100vh;
}

.side svg {
  width: 23px;
  height: 23px;
  fill: #a7a7a6;
  cursor: pointer;
  transition: 0.2s;
}

.side svg:hover {
  fill: white;
  background-color: #f08a47;
  border-radius: 5px;
  box-shadow: 0px 0px 0px 10px #f08a47;
}

img {
  width: 40px;
  margin-bottom: 20px;
}
</style>
