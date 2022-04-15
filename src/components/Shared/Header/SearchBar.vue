<template>
  <div style="display:flex;justify-content:space-between">
    <div class="search-bar">
      <div class="search-button">
        <v-icon class="arrow-right" name="arrow-right"></v-icon>
      </div>
      <div class="search">
        <v-icon class="search-glass" name="search"></v-icon>
        <input
          class="search-input"
          type="text"
          name="Search"
          placeholder="Search"
        />
      </div>
    </div>
    <div>
      <img src="../../../assets/avatar.png" alt="avatar" />
    </div>
  </div>
</template>

<script>
import Icon from "vue-awesome/components/Icon";
import "vue-awesome/icons/arrow-right";
import "vue-awesome/icons/search";

export default {
  components: {
    "v-icon": Icon
  }
};
</script>

<style scoped>
.search-bar {
  display: flex;
  align-items: center;
  column-gap: 20px;
  padding: 10px;
  margin-left: 5px;
}

.search {
  position: relative;
}

.search-glass {
  position: absolute;
  top: 50%;
  left: 10px;
  transform: translateY(-50%);
  fill: #a7a7a6;
  width: 15px;
  height: 15px;
}

.search-input {
  padding: 10px;
  padding-left: 33px;
  border-radius: 20px;
  outline: none;
  border: none;
  font-family: "Poppins", sans-serif;
}

.arrow-right {
  fill: #f08a47;
  border-radius: 50%;
  background: white;
  box-shadow: 0px 0px 0px 5px white;
  cursor: pointer;
  transition: 0.3s;
}
.arrow-right:hover {
  box-shadow: 0px 0px 0px 5px white, 0px 0px 0px 10px #f08a47;
}
img {
  width: 60px;
  border-radius: 50%;
}
</style>
