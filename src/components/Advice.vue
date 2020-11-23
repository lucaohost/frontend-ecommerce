<template>
  <div
    id="advice"
    class="font-size-tiny display-flex justify-content-center align-items-center white bg-light-black-1"
  >
    <span id="advice-text">
      Acompanhe as melhores promoções disponíveis aqui na Maeztra
    </span>
  </div>
</template>

<script>
export default {
  name: "Advice",
  props: {
    msg: String,
  },
};
</script>

<style lang="scss" scoped>
#advice {
  height: 24px;
  font-weight: 400;
}

#advice-text {
  @media (max-width: 768px) {
    font-size: 10px;
  }
}
</style>
