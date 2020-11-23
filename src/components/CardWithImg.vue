<template>
  <div
    id="card"
    class="font-size-tiny display-flex justify-content-center align-items-center light-black-1 bg-dark-white-2 border-radius-xtiny"
  >
    <img
      v-if="img == 'world'"
      src="../assets/world.svg"
      alt="Imagem de planeta"
      id="img"
    />
    <img
      v-else-if="img == 'stock'"
      src="../assets/stock.svg"
      alt="Imagem de estoque"
      id="img"
    />
    <img
      v-else-if="img == 'change'"
      src="../assets/change.svg"
      alt="Imagem de troca"
      id="img"
    />
    <img
      v-else-if="img == 'tag'"
      src="../assets/tag.svg"
      alt="Imagem de tag"
      id="img"
    />
    <img
      v-else-if="img == 'truck'"
      src="../assets/truck.svg"
      alt="Imagem de caminhão"
      id="img"
    />
    <span id="msg">
      <strong class="font-size-tiny"> {{ msg }}</strong> <br />
      <span font-size-normal>{{ subMsg }}</span>
    </span>
  </div>
</template>

<script>
export default {
  name: "CardWithImg",
  props: {
    msg: String,
    subMsg: String,
    img: String,
  },
};
</script>

<style scoped lang="scss">
#msg {
  padding-top: 18px;
  padding-bottom: 18px;
}
#img {
  margin-right: 22px;
}
#card {
  width: 308px;
  margin: 0px;
  @media (max-width: 768px) {
    width: 298px;
  }
}
</style>
