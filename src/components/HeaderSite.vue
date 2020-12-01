<template>
  <div
    class="header bg-white display-flex align-items-center justify-content-center"
  >
    <div class="display-flex align-items-center">
      <div class="div-menu">
        <Slide class="menu" width="200">
          <a href="#" v-for="(categorie, index) in categories" :key="index">
            <span class="font-size-medium">{{ categorie }}</span>
          </a>
        </Slide>
      </div>
      <img
        v-if="!iconSearchClicked"
        class="logo"
        src="../assets/logo.svg"
        alt="Logo Maeztra"
      />
    </div>
    <transition name="fade">
      <InputWithButton
        v-if="!iconSearchClicked"
        msg="O Que Você Busca?"
        textButton="Buscar"
        :search="true"
      />
    </transition>
    <IconWithText class="account" text="Minha Conta" icon="account" />
    <IconWithText class="heart" text="Minha Conta" icon="heart" />
    <transition name="fade">
      <div v-if="iconSearchClicked">
        <input
          class="border-radius-medium bg-dark-white-2 border-none input-search-mobile"
          type="text"
          v-on-clickaway="away"
        />
      </div>
    </transition>
    <img
      class="search"
      src="../assets/search-icon.svg"
      alt="Ícone de Busca"
      v-on:click="iconSearchClicked = true"
    />
    <div v-if="!iconSearchClicked" class="display-flex align-items-center">
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
import { Slide } from "vue-burger-menu";
import InputWithButton from "./InputWithButton";
import IconWithText from "./IconWithText";
import { mixin as clickaway } from "vue-clickaway";
export default {
  mixins: [clickaway],
  name: "HeaderSite",
  props: {
    msg: String,
  },
  data() {
    return {
      iconSearchClicked: false,
      categories: [
        "Minha Conta",
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
    InputWithButton,
    IconWithText,
    Slide,
  },
  methods: {
    away: function() {
      if (document.querySelector(".input-search-mobile") !== null) {
        console.log("clicked away");
        this.iconSearchClicked = false;
      }
    },
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
    position: absolute;
    left: -25px;
    top: 18px;
  }
}

.div-menu {
  margin-right: 55px;
}

.header {
  padding: 24px 0px;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.08);
  z-index: 1;
  @media (max-width: 900px) {
    padding: 32px 15px;
  }
  @media (max-width: 768px) {
    justify-content: right;
  }
}

.input-search-mobile {
  padding: 5px;
  margin-right: 5px;
  width: 250px;
}

.bag {
  width: 24px;
}

.fade-enter-active {
  transition: opacity 1s;
}

.fade-leave-active {
  transition: opacity 0s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
