<template>
  <va-accordion style="width: auto heigth: auto display: flex">
    <va-collapse color="#A6B1E1" header="основные продукты">
      <div @click="addToList">
        <button type="button">
          <img class="img" src="@/assets/сыр.png" name="сыр" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/грибы.png" name="грибы" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/курица.png" name="курица" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/мясо.png" name="мясо" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/мороженое.png" name="мороженое" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/печенье.png" name="печенье" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/сладости.png" name="сладости" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/сахар.png" name="сахар" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/рыба.png" name="рыба" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/хлеб.png" name="хлеб" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/яйца.png" name="яйца" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/алкоголь.png" name="алкоголь" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/вино.png" name="вино" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/пиво.png" name="пиво" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/газировка.png" name="газировка" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/крупы.png" name="крупы" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/мука.png" name="мука" />
        </button>
      </div>
    </va-collapse>

    <va-collapse color="#A6B1E1" header="овощи">
      <div @click="addToList">
        <button type="button">
          <img class="img" src="@/assets/морковь.png" name="морковь" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/баклажаны.png" name="баклажаны" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/горох.png" name="горох" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/капуста.png" name="капуста" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/кукуруза.png" name="кукуруза" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/перец.png" name="перец" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/помидоры.png" name="помидоры" />
        </button>
      </div>
    </va-collapse>

    <va-collapse color="#A6B1E1" header="фрукты">
      <div @click="addToList">
        <button type="button">
          <img class="img" src="@/assets/яблоки.png" name="яблоки" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/авокадо.png" name="авокадо" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/апельсин.png" name="апельсин" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/арбуз.png" name="арбуз" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/бананы.png" name="бананы" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/виноград.png" name="виноград" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/вишня.png" name="вишня" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/голубика.png" name="голубика" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/груша.png" name="груша" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/киви.png" name="киви" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/клубника.png" name="клубника" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/лимон.png" name="лимон" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/слива.png" name="слива" />
        </button>
      </div>
    </va-collapse>

    <va-collapse color="#A6B1E1" header="товары для дома">
      <div @click="addToList">
        <button type="button">
          <img class="img" src="@/assets/бумага.png" name="туалетная бумага" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/мыло.png" name="мыло" />
        </button>
        <button type="button">
          <img class="img" src="@/assets/паста.png" name="зубная паста" />
        </button>
        <button type="button">
          <img
            class="img"
            src="@/assets/порошок.png"
            name="стиральный порошок"
          />
        </button>
      </div>
    </va-collapse>
  </va-accordion>
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