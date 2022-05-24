<template>
  <div>
    <div class="title__block" style="margin-bottom: 10px">
      <h3 class="display-3">Список покупок</h3>
      <va-button @click.stop="$emit('removeAll')" color="#985F6F" size="small"
        >очистить список</va-button
      >
    </div>
    <transition-group name="purchases-list">
      <to-buy-element
        v-for="item in purchasesList"
        :item="item"
        :key="item.id"
        @remove="$emit('remove', item)"
        @toggleDone="$emit('toggleDone', item)"
      />
    </transition-group>
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
.purchases-list-item {
  display: inline-block;
  margin-right: 10px;
}
.purchases-list-enter-active,
.purchases-list-leave-active {
  transition: all 0.4s ease;
}
.purchases-list-enter-from,
.purchases-list-leave-to {
  opacity: 0;
  transform: translateY(30px);
}
.purchases-list-move {
  transition: transform 0.8s ease;
}

.title__block {
  display: flex;
  justify-content: space-between;
}
</style>