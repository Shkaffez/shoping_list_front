<template>
  <div>
    <add-to-list-form @add="add" />
    <to-buy-list
      :purchasesList="purchasesList"
      @remove="remove"
      @turnDone="turnDone"
    />
  </div>
</template>

<script>
import addToListForm from "@/components/addToListForm";
import toBuyList from "@/components/toBuyList";
export default {
  data() {
    return {
      purchasesList: [
        {
          id: 123,
          text: "test",
        },
        {
          id: 124,
          text: "test",
        },
        {
          id: 125,
          text: "test",
        },
      ],
    };
  },
  methods: {
    add(item) {
      this.purchasesList.push(item);
    },
    remove(item) {
      this.purchasesList = this.purchasesList.filter((el) => el.id !== item.id);
    },
    turnDone(item) {
      
    }
  },
  components: {
    addToListForm,
    toBuyList,
  },
};
</script>

<style>
</style>
