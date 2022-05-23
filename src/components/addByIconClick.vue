<template>
  <div @click="addToList">
    <button type="button">
      <img class="img" src="@/assets/морковь.png" name="морковь" />
    </button>
    <button type="button">
      <img class="img" src="@/assets/сыр.png" name="сыр" />
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    addToList(event) {
      this.$emit("add", {
        id: Date.now(),
        text: event.target.name,
        done: false,
      });
    },
  },
};
</script>

<style>
.img {
  width: 40px;
  height: 40px;
}
</style>