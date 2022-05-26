<template>
  <div
    @click="$emit('toggleDone', item)"
    class="toByItem"
    :class="{ done: item.done }"
  >
    <div class="text" :class="{ crossedOut: item.done }">{{ item.text }}</div>
    <va-button
      @click.stop="$emit('remove', item)"
      icon="block"
      color="#985F6F"
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
}
.text {
  padding: 5px;
}

.done {
  background: #fff5d7;
  opacity: 0.4;
}
.crossedOut {
  text-decoration: line-through;
}
</style>