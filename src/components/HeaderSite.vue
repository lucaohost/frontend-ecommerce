<template>
  <div
    class="header bg-white display-flex align-items-center justify-content-center"
  >
    <div class="display-flex align-items-center">
      <img class="menu" src="../assets/menu-icon.svg" alt="Menu" />
      <img class="logo" src="../assets/logo.svg" alt="Logo Maeztra" />
    </div>
    <InputWithButton
      msg="O Que Você Busca?"
      textButton="Buscar"
      :search="true"
    />
    <IconWithText class="account" text="Minha Conta" icon="account" />
    <IconWithText class="heart" text="Minha Conta" icon="heart" />
    <div class="display-flex align-items-center">
      <img
        class="search"
        src="../assets/search-icon.svg"
        alt="Ícone de Busca"
      />
      <img class="bag" src="../assets/bag-icon.svg" alt="Ícone de Sacola" />
    </div>
    <button
      class="buttton-carrinho display-flex border-radius-tiny black-light-2 font-size-normal bg-white align-items-center"
    >
      <img
        class="icon-bag-button"
        src="../assets/bag-icon.svg"
        alt="Ícone de Sacola"
      />
      <p>Meu Carrinho</p>
    </button>
  </div>
</template>

<script>
import InputWithButton from "./InputWithButton";
import IconWithText from "./IconWithText";
export default {
  name: "HeaderSite",
  props: {
    msg: String,
  },
  components: {
    InputWithButton,
    IconWithText,
  },
};
</script>

<style lang="scss" scoped>
img {
  height: 18px;
}
.logo {
  margin-right: 93px;
  @media (max-width: 1660px) {
    margin-right: 81.84px;
  }
  @media (max-width: 1480px) {
    margin-right: 72px;
  }
  @media (max-width: 1200px) {
    margin-right: 63.36px;
  }
  @media (max-width: 1040px) {
    margin-right: 55.7px;
  }
  @media (max-width: 900px) {
    margin-right: 20px;
  }
}

.account {
  margin-left: 147px;
  @media (max-width: 1660px) {
    margin-left: 96px;
  }
  @media (max-width: 1480px) {
    margin-left: 30px;
  }
  @media (max-width: 1200px) {
    margin-left: 10px;
  }
  @media (max-width: 1040px) {
    margin-left: 5px;
  }
  @media (max-width: 768px) {
    display: none;
  }
  @media (max-width: 576px) {
    display: none;
  }
}

.buttton-carrinho {
  border-color: #f3ba49;
  height: 55px;
  border-style: solid;

  @media (max-width: 768px) {
    display: none;
  }
}

.heart {
  margin-left: 8px;
  margin-right: 50px;
  @media (max-width: 1660px) {
    margin-right: 40px;
  }
  @media (max-width: 1480px) {
    margin-right: 32px;
  }
  @media (max-width: 1200px) {
    margin-right: 15px;
  }
  @media (max-width: 900px) {
    margin-right: 7.5px;
  }
  @media (max-width: 768px) {
    display: none;
  }
  @media (max-width: 576px) {
    display: none;
  }
}

.search {
  @media (min-width: 769px) {
    display: none;
  }
  @media (max-width: 768px) {
    display: block;
    margin-right: 32px;
    width: 24px;
    height: 24px;
  }
}

.icon-bag-button {
  margin-right: 5px;
}

.bag {
  @media (min-width: 769px) {
    display: none;
  }
  @media (max-width: 768px) {
    display: block;
    width: 20.77px;
    height: 24px;
  }
}

.menu {
  @media (min-width: 769px) {
    display: none;
  }
  @media (max-width: 768px) {
    display: block;
    width: 24px;
    height: 24px;
    margin-right: 19px;
  }
}

.header {
  padding: 24px 0px;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.08);
  z-index: 1;
  @media (max-width: 900px) {
    padding: 32px 15px;
  }
  @media (max-width: 768px) {
    justify-content: space-between;
  }
}

.bag {
  width: 24px;
}
</style>
