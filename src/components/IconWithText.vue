<template>
  <div class="display-flex">
    <img
      v-if="icon == 'account'"
      src="../assets/account-icon.svg"
      alt="Ícone de Usuário"
    />
    <img
      v-else-if="icon == 'heart'"
      src="../assets/heart-icon.svg"
      alt="Ícone de Coração"
    />
    <img
      v-else-if="icon == 'bag'"
      src="../assets/bag-icon.svg"
      alt="Ícone de Sacola"
    />
    <img
      v-else-if="icon == 'dress'"
      src="../assets/dress-icon.svg"
      alt="Ícone de Sacola"
      class="dress"
    />
    <span class=" font-size-normal" :class="textColor">{{ text }}</span>
  </div>
</template>

<script>
export default {
  name: "IconWithText",
  props: {
    text: String,
    icon: String,
    textColor: {
      type: String,
      default: "light-black-1",
    },
  },
};
</script>

<style scoped lang="scss">
img {
  margin-right: 8px;
}
.dress {
  height: 15px;
  width: 12px;
}
</style>
