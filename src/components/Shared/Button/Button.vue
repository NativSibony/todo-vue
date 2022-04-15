<template>
  <button class="btn" :class="color">{{ tagName }}</button>
</template>

<script>
export default {
  props: {
    tagName: String,
    color: String
  }
};
</script>

<style scoped>
.btn {
  border: none;
  border-radius: 10px;
  padding: 6px 10px;
  cursor: pointer;
}
.btn.blue {
  background-color: #e5ecf7;
  color: #6690d3;
}
.btn.green {
  background-color: #e7f1e8;
  color: #54ad70;
}
.btn.red {
  background-color: #f5e7e7;
  color: #ce7979;
}
.btn.purple {
  background-color: #efe9f3;
  color: #7d709c;
}
</style>
