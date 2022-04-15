<template>
  <div class="menu" :class="showMenu ? 'active' : ''" >
    <p>Edit</p>
    <p>Priority</p>
  </div>
</template>

<script>
export default {
  props: {
    showMenu: Boolean
  }
};
</script>

<style scoped>
.menu {
  position: absolute;
  background-color: white;
  font-size: 0px;
  height: 0;
  width: 200px;
  overflow: hidden;

  border-radius: 10px;
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;

  transition: 0.4s;
}

.menu.active {
  font-size: 14px;
  height: 85px;
}

p {
  font-size: 0.6rem;
  padding: 10px;
  cursor: pointer;
}

p:hover {
  border-radius: 10px;
  background-color: #eee;
}
</style>
