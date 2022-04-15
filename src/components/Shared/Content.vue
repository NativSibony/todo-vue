<template>
  <div class="content">
    <div class="col" id="todo">
      <div class="title">
        <v-icon name="circle" fill="#6690d3"></v-icon>
        <h4>{{ title.toDo }}</h4>
      </div>
      <app-card
        v-for="todo in cData.todo"
        :key="todo.id"
        :cardTitle="todo.title"
        :cardContent="todo.content"
        :cardDate="todo.dateAdded"
      />
    </div>
    <div class="col" id="inprogress">
      <div class="title">
        <v-icon name="circle" fill="#f08a47"></v-icon>
        <h4>{{ title.inProgress }}</h4>
      </div>
      <app-card
        v-for="inprogress in cData.inprogress"
        :key="inprogress.id"
        :cardTitle="inprogress.title"
        :cardContent="inprogress.content"
        :cardDate="inprogress.dateAdded"
      />
    </div>
    <div class="col" id="completed">
      <div class="title">
        <v-icon name="circle" fill="#54ad70"></v-icon>
        <h4>{{ title.completed }}</h4>
      </div>
      <app-card
        v-for="completed in cData.completed"
        :key="completed.id"
        :cardTitle="completed.title"
        :cardContent="completed.content"
        :cardDate="completed.dateAdded"
      />
    </div>
  </div>
</template>

<script>
import Card from "./Card/Card.vue";
import Icon from "vue-awesome/components/Icon";
import "vue-awesome/icons/circle";

export default {
  data() {
    return {
      title: {
        toDo: "To Do",
        inProgress: "In Progress",
        completed: "Completed"
      },
      cardTitle: "Stom Ta Tahat",
      cardContent: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ullam nemo,
        mollitia animi eum fugiat odit architecto possimus libero error tempore
        dolor nostrum doloribus. Incidunt, fugiat.`,
      cardDate: this.getDate(),
      cData: {}
    };
  },
  components: {
    "v-icon": Icon,
    "app-card": Card
  },
  methods: {
    getDate() {
      var today = new Date();
      var dd = String(today.getDate()).padStart(2, "0");
      var mm = String(today.getMonth() + 1).padStart(2, "0"); //January is 0!
      var yyyy = today.getFullYear();

      return dd + "/" + mm + "/" + yyyy;
    },
    fetchData() {
      fetch("http://localhost:8080/static/data.json")
        .then(response => response.json())
        .then(data => (this.cData = data));
    }
  },
  created() {
    this.fetchData();
  }
};
</script>

<style scoped>
.content {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
.col {
  padding: 10px;
  display: flex;
  flex-direction: column;
  row-gap: 20px;
}

.title {
  display: flex;
  align-items: center;
  column-gap: 10px;
}

.title h4 {
  font-weight: 500;
  font-size: 1rem;
}

svg {
  width: 11px;
  height: 11px;
}
</style>
