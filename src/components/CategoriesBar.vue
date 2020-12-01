<template>
  <div
    id="categories-bar"
    class="display-flex align-items-center justify-content-center"
  >
    <ul class="display-flex">
      <li
        v-for="(categorie, index) in categories"
        :class="'categorie ' + (index == 0 ? 'primary' : '')"
        :key="index"
        v-on:click="clickCategorie(categorie)"
      >
        {{ categorie }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "CategoriesBar",
  data() {
    return {
      categories: [
        "Novidades",
        "Vestidos",
        "Roupas",
        "Sapatos",
        "Lingerie",
        "Acessórios",
        "OUTLET",
      ],
    };
  },
  methods: {
    clickCategorie(categorieClicked) {
      let categories = document.querySelectorAll(".categorie");
      for (let i = 0; i < categories.length; i++) {
        if (categories[i].innerHTML.trim() == categorieClicked) {
          categories[i].classList.add("primary");
        } else {
          categories[i].classList.remove("primary");
        }
      }
    },
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
