<template>
  <div class="container">
    <add-to-list-form @add="add" style="margin-top: 10px" />
    <add-by-icon-click @add="add" />
    <to-buy-list
      :purchasesList="purchasesList"
      @remove="remove"
      @removeAll="removeAll"
      @toggleDone="toggleDone"
      class="toByList"
    />
  </div>
</template>

<script>
import addToListForm from "@/components/addToListForm";
import toBuyList from "@/components/toBuyList";
import addByIconClick from "@/components/addByIconClick";
export default {
  data() {
    return {
      purchasesList: [],
    };
  },
  methods: {
    add(item) {
      this.purchasesList.push(item);
    },
    remove(item) {
      this.purchasesList = this.purchasesList.filter((el) => el.id !== item.id);
    },

    removeAll() {
      this.purchasesList = [];
    },

    toggleDone(item) {
      let el = this.purchasesList.find((row) => row.id === item.id);
      el.done = !el.done;
    },
  },
  components: {
    addToListForm,
    toBuyList,
    addByIconClick,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  padding: 0 15px;
}

@media (min-width: 575.98px) {
  .container {
    max-width: 540px;
    margin: auto;
    padding: 0;
  }
}

@media (min-width: 767.98px) {
  .container {
    max-width: 720px;
  }
}

@media (min-width: 991.98px) {
  .container {
    max-width: 960px;
  }
}

@media (min-width: 1199.98px) {
  .container {
    max-width: 1140px;
  }
}

.toByList {
  margin-top: 20px;
}
</style>
