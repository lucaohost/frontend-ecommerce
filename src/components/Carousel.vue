<template>
  <div id="carousel">
    <div class="divPromocoes">
      <p id="promotion" class="white font-size-xl font-weight-bold">
        Promoções de Outono
      </p>
    </div>
    <div class="display-flex">
      <img
        id="arrow-left"
        src="../assets/left.svg"
        alt="Flecha para esquerda"
      />
      <p id="promotionText" class="white font-size-big">
        Confiras os melhores looks para combinar com você nesse Outono
      </p>
      <img
        id="arrow-right"
        src="../assets/right.svg"
        alt="Flecha para direita"
      />
    </div>
    <div>
      <button
        class="border-radius-tiny bg-primary white border-none font-size-normal font-weight-bold"
      >
        Conferir
      </button>
    </div>
    <div class="display-flex justify-content-center align-items-center balls">
      <img id="ball" src="../assets/ball.svg" alt="" />
      <img id="circle" src="../assets/circle.svg" alt="" />
      <img id="circle" src="../assets/circle.svg" alt="" />
      <img id="circle" src="../assets/circle.svg" alt="" />
      <img id="circle" src="../assets/circle.svg" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Carousel",
  props: {
    msg: String,
  },
};
</script>

<style lang="scss" scoped>
#carousel {
  background-image: url("../assets/carousel.svg");
  background-repeat: no-repeat;
  height: 600px;
  margin-right: 0px;
  @media (max-width: 670px) {
    height: 320px;
    background-size: 656px 312px;
  }
  @media (max-width: 670px) {
    height: 320px;
    background-size: 656px 312px;
  }
}
.divPromocoes {
  @media (max-width: 768px) {
    width: 280px;
  }
}

#promotion {
  padding-top: 151px;
  padding-left: 310px;
  margin: 0px;
  @media (max-width: 768px) {
    padding-top: 63px;
    padding-left: 74px;
    font-size: 30px;
  }
}
#promotionText {
  margin-left: 125px;
  width: 380px;
  margin-top: 40px;
  @media (max-width: 768px) {
    margin-left: 0px;
    font-size: 14px;
    width: 210px;
    padding-left: 19px;
    margin-top: 12px;
  }
}
button {
  padding-top: 14px;
  padding-bottom: 14px;
  padding-right: 37px;
  padding-left: 37px;
  margin-left: 310px;
  margin-top: 5px;
  @media (max-width: 768px) {
    margin-top: 0px;
    padding-top: 6px;
    padding-bottom: 6px;
    padding-right: 11px;
    padding-left: 11px;
    margin-left: 74px;
  }
}

#arrow-left {
  margin-left: 164px;
  @media (max-width: 768px) {
    margin-left: 37px;
  }
}

#arrow-right {
  margin-left: 1038px;
  @media (max-width: 1750px) {
    margin-left: 800px;
  }
  @media (max-width: 1450px) {
    margin-left: 600px;
  }
  @media (max-width: 1260px) {
    margin-left: 400px;
  }
  @media (max-width: 1120px) {
    margin-left: 200px;
  }
  @media (max-width: 875px) {
    margin-left: 100px;
  }
  @media (max-width: 768px) {
    margin-left: 50px;
  }
}

#ball {
  margin-right: 16px;
  @media (max-width: 768px) {
    height: 8px;
    width: 8px;
    margin-top: 40px;
  }
}

#circle {
  margin-right: 16px;
  @media (max-width: 768px) {
    height: 8px;
    width: 8px;
    margin-top: 40px;
  }
}

.balls {
  margin-top: 200px;
  @media (max-width: 768px) {
    margin-top: 0px;
  }
}
</style>
