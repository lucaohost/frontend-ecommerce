<template>
  <div class="bg-white display-flex align-items-center">
    <input
      id="inputText"
      :class="{
        'input-search border-radius-medium bg-dark-white-2 border-none': search,
        'input-newsletter border-radius-tiny1': !search,
      }"
      type="text"
      :placeholder="msg"
    />
    <button
      :class="{
        'font-size-normal button-search': search,
        'font-size-medium font-weight-bold button-newsletter': !search,
      }"
      class="border-radius-tiny bg-primary white border-none"
    >
      {{ textButton }}
    </button>
  </div>
</template>

<script>
export default {
  name: "InputWithButton",
  props: {
    msg: String,
    textButton: String,
    search: Boolean,
  },
};
</script>

<style lang="scss" scoped>
button {
  padding-right: 38px;
  padding-left: 38px;
}

.button-search {
  margin-left: -15px;
  padding-top: 14px;
  padding-bottom: 14px;
  @media (max-width: 768px) {
    display: none;
  }
}

.input-search {
  padding-top: 13px;
  padding-bottom: 13px;
  padding-left: 24px;
  padding-right: 24px;
  width: 672px;
  @media (max-width: 1660px) {
    width: 600px;
  }
  @media (max-width: 1480px) {
    width: 435px;
  }
  @media (max-width: 1200px) {
    width: 320px;
  }
  @media (max-width: 1040px) {
    width: 280px;
  }
  @media (max-width: 992px) {
    width: 200px;
  }
  @media (max-width: 768px) {
    display: none;
  }
}

.input-newsletter {
  width: 500px;
  border: 1px solid #353535;
  padding: 12px 24px;

  @media (max-width: 768px) {
    width: 200px;
    padding: 5px 24px;
  }
}

.button-newsletter {
  margin-left: -15px;
  padding-top: 14px;
  padding-bottom: 14px;
  @media (max-width: 768px) {
    margin-left: 15px;
    padding-top: 5px;
    padding-bottom: 5px;
  }
}
</style>
