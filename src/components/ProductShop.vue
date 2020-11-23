<template>
  <div class="productShop">
    <img
      v-if="product == 'product1'"
      src="../assets/product1.svg"
      alt="Imagem de Produto"
    />
    <img
      v-else-if="product == 'product2'"
      src="../assets/product2.svg"
      alt="Imagem de Produto"
    />
    <div class="colors display-flex">
      <div
        v-for="color in colors"
        :key="color"
        :class="'color-block bg-' + color + ' border-radius-tiny1'"
      ></div>
    </div>
    <div class="product-infos">
      <p class="font-size-big font-weight-bold">{{ price }}</p>
      <p class="font-size-medium font-weight-semibold">{{ name }}</p>
      <p v-if="product == 'product1'" class="font-size-tiny break-description">
        {{ description }}
      </p>
      <p v-if="product == 'product2'" class="font-size-tiny">
        {{ description }}
      </p>
    </div>
    <div class="display-flex justify-content-center align-items-center">
      <button
        class="border-radius-tiny1 bg-primary white border-none font-size-medium"
      >
        Adicionar
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductShop",
  props: {
    product: String,
    colors: [],
    price: String,
    name: String,
    description: String,
  },
};
</script>

<style scoped lang="scss">
.color-block {
  width: 27px;
  height: 27px;
  margin-top: 4px;
}
.productShop {
  width: 308px;
}
.colors,
.product-infos {
  margin-left: 27px;
}

.color-block {
  margin-right: 8px;
}
button {
  padding-right: 94px;
  padding-left: 94px;
  padding-top: 8px;
  padding-bottom: 8px;
}

.break-description {
  padding-right: 40px;
}
</style>
