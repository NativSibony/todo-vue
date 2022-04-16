<template>
  <div class="card">
    <div class="card-header">
      <div>{{ cardTitle }}</div>
      <div>
        <v-icon class="ellipsis" name="ellipsis-h" @click="toggleMenu"></v-icon>
        <app-card-menu :showMenu="showMenu"></app-card-menu>
      </div>
    </div>
    <div class="card-body">
      <div class="tags">
        <app-button color="blue" :tagName="tagName"></app-button>
        <app-button color="green" :tagName="tagName"></app-button>
      </div>
      <p>
        {{ cardContent }}
      </p>
    </div>
    <div class="card-footer">
      <div class="date">
        <v-icon name="calendar-alt" class="calendar"></v-icon>
        <p>{{ cardDate }}</p>
      </div>
      <div class="asginee"></div>
    </div>
  </div>
</template>

<script>
import CardMenu from "./CardMenu.vue";
import Button from "../Button/Button.vue";
import Icon from "vue-awesome/components/Icon";
//name of icon will be taken from 'font awesome' alias name
import "vue-awesome/icons/ellipsis-h";
import "vue-awesome/icons/calendar-alt";

export default {
  data() {
    return {
      tagName: "Shalom",
      showMenu: false
      // rightToggle: true
    };
  },
  props: {
    cardTitle: String,
    cardContent: String,
    cardDate: String
  },
  components: {
    "app-button": Button,
    "app-card-menu": CardMenu,
    "v-icon": Icon
  },
  methods: {
    toggleMenu() {
      this.showMenu = !this.showMenu;
    }
  }
};
</script>

<style scoped>
.ellipsis:hover {
  cursor: pointer;
  fill: #f08a47;
}
.card {
  display: flex;
  flex-direction: column;
  background-color: #fff;
  padding: 15px;
  border-radius: 10px;
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
  transition: 0.4s;
}
.card-header {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  font-size: 0.9rem;
  font-weight: 600;
  color: #333;
}

.card-body {
  color: #a7a7a6;
  font-size: 0.7rem;
}

.card-footer {
  margin-top: 20px;
}

.calendar {
  width: 18px;
  height: 18px;
}

.tags {
  margin-bottom: 15px;
}

.date {
  display: flex;
  align-items: center;
  column-gap: 15px;
}
.date p {
  color: #666;
  font-size: 0.6rem;
  padding-top: 2.5px;
}

svg {
  fill: #bbb;
  width: 25px;
  height: 25px;
  stroke: white;
  stroke-width: 25px;
}
</style>
