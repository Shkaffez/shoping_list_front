<template>
  <div @click="$emit('turnDone', item)" class="toByItem">
    <div class="text">{{ item.text }}</div>
    <va-button
      @click.stop="$emit('remove', item)"
      icon="block"
      color="danger"
      size="small"
    />
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
    },
  },
};
</script>

<style>
.toByItem {
  display: flex;
  justify-content: space-between;
  border: 2px solid #2c82e0;
  margin-bottom: 2px;
  width: 500px;
}
.text {
  padding: 5px;
}
</style>