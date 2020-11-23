<template>
  <div
    id="categories-bar"
    class="display-flex align-items-center justify-content-center"
  >
    <IconWithText textColor="primary" text="Novidades" icon="dress" />
    <ul class="display-flex">
      <li v-for="(categorie, index) in categories" :key="index">
        {{ categorie }}
      </li>
    </ul>
  </div>
</template>

<script>
import IconWithText from "./IconWithText";
export default {
  name: "CategoriesBar",
  data() {
    return {
      categories: [
        "Vestidos",
        "Roupas",
        "Sapatos",
        "Lingerie",
        "Acessórios",
        "OUTLET",
      ],
    };
  },
  components: {
    IconWithText,
  },
};
</script>

<style lang="scss" scoped>
ul {
  list-style: none;
  padding: 0;
}
li {
  margin-left: 132px;
  @media (max-width: 1660px) {
    margin-left: 116px;
  }
  @media (max-width: 1480px) {
    margin-left: 100x;
  }
  @media (max-width: 1200px) {
    margin-left: 70px;
  }
  @media (max-width: 1040px) {
    margin-left: 40px;
  }
  @media (max-width: 768px) {
    margin-left: 15px;
  }
}
#categories-bar {
  @media (max-width: 576px) {
    display: none;
  }
}
</style>
