<template>
  <div class="display-flex justify-content-center content">
    <div class="list-div" v-for="menu in menus" :key="menu.name">
      <span class="font-size-medium font-weight-bold black-light-1">
        {{ menu.name }}
      </span>
      <ul>
        <li
          v-for="content in menu.content"
          :key="content"
          class="font-size-tiny"
        >
          {{ content }}
        </li>
      </ul>
    </div>
    <div class="list-div-mobile" v-for="menu in menus" :key="menu.name">
      <div class="menu-title display-flex justify-content-between">
        <span class="font-size-medium font-weight-bold black-light-1">
          {{ menu.name }}
        </span>
        <span
          v-if="!menu.show"
          v-on:click="menu.show = true"
          class="font-size-medium font-weight-bold black-light-1"
        >
          +
        </span>
        <span
          v-if="menu.show"
          v-on:click="menu.show = false"
          class="font-size-medium font-weight-bold black-light-1"
        >
          -
        </span>
      </div>
      <ul v-if="menu.show">
        <li
          v-for="content in menu.content"
          :key="content"
          class="font-size-tiny"
        >
          {{ content }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterMenu",
  data() {
    return {
      menus: [
        {
          name: "Informações",
          show: false,
          content: [
            "Quem Somos",
            "Prazo de Envio",
            "Troca e Devoluções",
            "Promoções e Cupons",
          ],
        },
        {
          name: "Minha Conta",
          show: false,
          content: ["Minha Conta", "Meus Pedidos", "Cadastre-se"],
        },
        {
          name: "Onde nos Encontrar",
          show: false,
          content: ["Lojas", "Endereço"],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
ul {
  list-style: none;
  padding: 0px;
  @media (max-width: 768px) {
    margin-top: 0px;
    margin-bottom: 20px;
  }
}

li {
  padding-top: 24px;
  @media (max-width: 768px) {
    padding-top: 10px;
  }
}

li:first-chil {
  padding-top: 24px;
  @media (max-width: 768px) {
    padding-top: 10px;
  }
}

.menu-title {
  margin-bottom: 17px;
}

.content {
  padding: 40px;
  @media (max-width: 768px) {
    flex-direction: column;
  }
}

.list-div:first-child {
  padding-left: 0px;
}

.list-div {
  padding-left: 361px;
  @media (max-width: 768px) {
    display: none;
  }
}

.list-div-mobile {
  display: none;
  @media (max-width: 768px) {
    display: block;
  }
}
</style>
