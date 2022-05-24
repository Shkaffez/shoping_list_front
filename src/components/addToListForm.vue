<template>
  <form @submit.prevent>
    <va-input
      class="mb-4"
      label="Добавить в список покупок"
      placeholder="например редиска"
      v-model="item.text"
    ></va-input>
    <va-button
      icon-right="create"
      @click="addToList"
      style="margin-bottom: 20px"
      color="#4E4C67"
      >Добавить</va-button
    >
  </form>
</template>

<script>
export default {
  data() {
    return {
      item: {
        text: "",
        id: undefined,
      },
    };
  },
  methods: {
    addToList() {
      this.item.id = Date.now();
      this.$emit("add", {
        id: this.item.id,
        text: this.item.text,
        done: false,
      });
      this.item.text = "";
    },
  },
};
</script>

<style>
</style>