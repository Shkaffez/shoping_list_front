<template>
  <div>
    <h2>Список покупок</h2>
    <ol>
      <to-buy-element
        v-for="item in purchasesList"
        :item="item"
        :key="item.id"
        @remove="$emit('remove', item)"
        @turnDone="$emit('turnDone', item)"
      />
    </ol>
  </div>
</template>

<script>
import toBuyElement from "@/components/toBuyElement.vue";
export default {
  props: {
    purchasesList: {
      type: Array,
      required: true,
    },
  },
  components: {
    toBuyElement,
  },
};
</script>

<style>
</style>