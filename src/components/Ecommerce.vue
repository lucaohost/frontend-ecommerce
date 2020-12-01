<template>
  <div class="ecommerce">
    <Advice />
    <HeaderSite />
    <CategoriesBar />
    <agile>
      <div class="slide" v-for="index in 5" :key="index">
        <img
          class="img-carousel"
          src="../assets/carousel.svg"
          alt="Modelo Posando"
        />
        <img
          class="img-carousel-mobile"
          src="../assets/carousel-mobile.svg"
          alt="Modelo Posando"
        />
      </div>
      <template slot="nextButton"
        ><img src="../assets/right.svg" alt="Flexa para direita"
      /></template>
      <template slot="prevButton"
        ><img src="../assets/left.svg" alt="Flexa para esquerda"
      /></template>
    </agile>
    <h1 class="white carousel-texts">Promoções de Outono</h1>
    <p class="white carousel-sub-texts">
      Confiras os melhores looks para combinar com você nesse Outono
    </p>
    <input
      type="button"
      class="button-carrousel white border-none font-weight-bold"
      value="Conferir"
    />
    <h2
      class="display-flex font-size-medium justify-content-center align-items-center font-weight-bold"
    >
      Por que comprar na Maeztra?
    </h2>
    <ul
      class="display-flex justify-content-center align-items-center scroll-x cards"
    >
      <li v-for="card in cards" :key="card.img">
        <CardWithImg :msg="card.msg" :subMsg="card.subMsg" :img="card.img" />
      </li>
    </ul>
    <h2
      id="marcasH2"
      class="display-flex font-size-xxbig justify-content-center align-items-center font-weight-bold"
    >
      Marcas Parceiras
    </h2>
    <div
      id="marcasParceiras"
      class="scroll-x display-flex justify-content-center align-items-center"
    >
      <img src="../assets/comma-logo.svg" alt="Logo Comma" />
      <img src="../assets/melissa-logo.svg" alt="Logo Melissa" />
      <img src="../assets/forever-21-logo.svg" alt="Logo Forever 21" />
      <img src="../assets/zara-logo.svg" alt="Logo Zara" />
      <img src="../assets/ann-taylor-logo.svg" alt="Logo Ann Taylor" />
    </div>
    <h2
      class="display-flex font-size-xxbig justify-content-center align-items-center font-weight-bold"
    >
      As Mais Pedidas
    </h2>
    <div
      class="products display-flex justify-content-center align-items-center scroll-x"
    >
      <ProductShop
        class="ProductShop"
        v-for="(productShop, index) in products"
        :key="index"
        :product="productShop.product"
        :price="productShop.price"
        :name="productShop.name"
        :description="productShop.description"
        :colors="productShop.colors"
      />
    </div>
    <div
      class="second-img-div display-flex align-items-center 
  justify-content-center"
    >
      <TitleWithText />
      <img
        class="second-img"
        src="../assets/second-img.svg"
        alt="Segunda Imagem"
      />
    </div>
    <div
      class="newsletter display-flex justify-content-center align-items-center"
    >
      <span class="newsletter-title font-size-xbig font-weight-bold">
        Receba Nossa Newsletter
      </span>
      <InputWithButton msg="Digite seu e-mail" textButton="Enviar" />
    </div>
    <FooterMenu />
    <Footer />
    <Modal v-if="showModal" @close="showModal = false" />
  </div>
</template>

<script>
import Advice from "./Advice.vue";
import HeaderSite from "./HeaderSite.vue";
import CategoriesBar from "./CategoriesBar.vue";
import CardWithImg from "./CardWithImg.vue";
import TitleWithText from "./TitleWithText.vue";
import ProductShop from "./ProductShop.vue";
import InputWithButton from "./InputWithButton.vue";
import FooterMenu from "./FooterMenu.vue";
import Footer from "./Footer.vue";
import Modal from "./Modal.vue";
import { VueAgile } from "vue-agile";

export default {
  name: "Ecommerce",
  components: {
    Advice,
    HeaderSite,
    CategoriesBar,
    CardWithImg,
    TitleWithText,
    ProductShop,
    InputWithButton,
    FooterMenu,
    Footer,
    Modal,
    agile: VueAgile,
  },
  data() {
    return {
      cards: [
        {
          msg: "Produtos Importados",
          subMsg: "Produtos de Alta Qualidade",
          img: "world",
        },
        {
          msg: "Estoque no Brazil",
          subMsg: "Produtos mais perto de você!",
          img: "stock",
        },
        {
          msg: "Trocas Garantidas",
          subMsg: "Trocas em até 48 horas, veja as regras",
          img: "change",
        },
        {
          msg: "Ganhe 5% off",
          subMsg: "Pagando à vista no Cartão",
          img: "tag",
        },
        {
          msg: "Frete Grátis",
          subMsg: "Em compras acima de R$499,00",
          img: "truck",
        },
      ],
      products: [
        {
          product: "product1",
          name: "Faux Suede Mini Skirt",
          description:
            "A faux suede mini skirt featuring exposed button-front closures and panel seam construction.",
          price: "R$ 500,00",
          colors: ["beige", "light-red", "light-blue", "dark-blue"],
        },
        {
          product: "product2",
          name: "Ruched Rose Print Mini Skirt",
          description:
            "A satin mini skirt featuring an allover floral print, ruched side with self-tie closure, concealed back zipper, and a flounce hem.",
          price: "R$ 320,00",
          colors: ["light-black", "red", "light-beige", "light-beige-1"],
        },
        {
          product: "product1",
          name: "Faux Suede Mini Skirt",
          description:
            "A faux suede mini skirt featuring exposed button-front closures and panel seam construction.",
          price: "R$ 500,00",
          colors: ["beige", "light-red", "light-blue", "dark-blue"],
        },
        {
          product: "product2",
          name: "Ruched Rose Print Mini Skirt",
          description:
            "A satin mini skirt featuring an allover floral print, ruched side with self-tie closure, concealed back zipper, and a flounce hem.",
          price: "R$ 320,00",
          colors: ["light-black", "red", "light-beige", "light-beige-1"],
        },
        {
          product: "product1",
          name: "Faux Suede Mini Skirt",
          description:
            "A faux suede mini skirt featuring exposed button-front closures and panel seam construction.",
          price: "R$ 500,00",
          colors: ["beige", "light-red", "light-blue", "dark-blue"],
        },
      ],
      showModal: true,
    };
  },
};
</script>

<style scoped lang="scss">
.cards {
  @media (max-width: 768px) {
    justify-content: normal;
    margin-right: 15px;
    margin-left: 15px;
  }
}

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.products {
  @media (max-width: 768px) {
    margin-bottom: 23px;
    justify-content: normal;
    margin-right: 15px;
    margin-left: 15px;
  }
}

.scroll-x {
  @media (max-width: 768px) {
    overflow-x: scroll;
  }
}

.second-img-div {
  margin: 0px 161px;
  @media (max-width: 1075px) {
    margin: 0px 31px;
    flex-direction: column;
  }
}

.second-img {
  height: 684px;
  width: 1114px;
  margin-left: 64px;
  margin-bottom: 80px;
  @media (max-width: 1680px) {
    margin-left: 0px;
    margin-bottom: 39px;
    margin-left: 34px;
    height: 505px;
    width: 800px;
  }
  @media (max-width: 1320px) {
    margin-left: 0px;
    margin-bottom: 29px;
    margin-left: 24px;
    height: 405px;
    width: 700px;
  }
  @media (max-width: 1225px) {
    margin-left: 0px;
    margin-bottom: 19px;
    margin-left: 14px;
    height: 505px;
    width: 600px;
  }
  @media (max-width: 1150px) {
    margin-left: 0px;
    margin-bottom: 9px;
    margin-left: 14px;
    height: 405px;
    width: 500px;
  }
  @media (max-width: 1090px) {
    margin-left: 0px;
    margin-bottom: 9px;
    margin-left: 14px;
    height: 305px;
    width: 400px;
  }

  @media (max-width: 768px) {
    margin-left: 0px;
    margin-bottom: 39px;
    height: 185px;
    width: 300px;
  }
}

.newsletter-title {
  margin-right: 39px;
  @media (max-width: 768px) {
    margin-bottom: 8px;
    margin-right: 0px;
  }
}

.newsletter {
  padding: 40px 0px;
  border-bottom: 2px solid #efefef;
  border-top: 2px solid #efefef;
  background-color: #fafafa;

  @media (max-width: 768px) {
    flex-direction: column;
  }
}

#marcasH2 {
  margin-top: 74px;
  margin-bottom: 17px;
}

#marcasParceiras {
  margin-bottom: 80px;
  @media (max-width: 768px) {
    justify-content: normal;
    margin-right: 15px;
    margin-left: 15px;
  }
}

.img-carousel {
  display: block;
  @media (max-width: 360px) {
    display: none;
  }
}

.img-carousel-mobile {
  display: none;
  @media (max-width: 360px) {
    display: block;
  }
}

.ProductShop {
  margin-right: 16px;
}

.carousel-texts {
  z-index: 1;
  position: absolute;
  left: 20rem;
  top: 19rem;
  font-size: 40px;
  @media (max-width: 1290px) {
    top: 15rem;
    left: 10rem;
    font-size: 30px;
  }
  @media (max-width: 768px) {
    top: 10rem;
    left: 4rem;
    width: 170px;
    font-size: 30px;
  }
}

.carousel-sub-texts {
  z-index: 1;
  position: absolute;
  left: 20rem;
  top: 400px;
  font-size: 20px;
  width: 390px;
  @media (max-width: 1290px) {
    top: 20rem;
    left: 10rem;
  }
  @media (max-width: 768px) {
    top: 15rem;
    width: 210px;
    left: 4rem;
    font-size: 14px;
  }
}

.button-carrousel {
  position: absolute;
  width: 128px;
  height: 48px;
  left: 323px;
  top: 500px;
  background: #faa500;
  border-radius: 10px;
  font-size: 16px;
  @media (max-width: 1290px) {
    font-size: 14px;
    width: 76px;
    height: 28px;
    left: 10rem;
    top: 25rem;
  }
  @media (max-width: 768px) {
    font-size: 14px;
    width: 76px;
    height: 28px;
    left: 4rem;
    top: 20rem;
  }
}
</style>

<style lang="sass">
// VueAgile styles
.agile
	&__nav-button
		background: transparent
		border: none
		color: #fff
		cursor: pointer
		font-size: 24px
		height: 100%
		position: absolute
		top: 0
		transition-duration: .3s
		width: 80px
		&--prev
			left: 0

		&--next
			right: 0

	&__dots
		bottom: 10px
		left: 50%
		position: absolute
		transform: translateX(-50%)

	&__dot
		margin: 0 10px

		button
			background-color: transparent
			border: 1px solid #FAA500
			border-radius: 50%
			cursor: pointer
			display: block
			height: 16px
			font-size: 0
			line-height: 0
			margin: 0
			padding: 0
			transition-duration: .3s
			width: 16px

		&--current,
		&:hover
			button
				background-color: #FAA500

// Slides styles
.slide
	display: block
	object-fit: cover
	width: 100%
</style>
