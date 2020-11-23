<template>
  <transition name="modal">
    <div class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
          <div class="display-flex close">
            <span class="white font-size-tiny" v-on:click="$emit('close')">
              FECHAR
            </span>
          </div>
          <div class="modal-body">
            <img class="img-modal" src="../assets/image-modal.png" alt="Menu" />
            <div
              class="display-flex align-items-center justify-content-center content"
            >
              <img src="../assets/mail-icon.svg" alt="Menu" />
              <span class="font-size-tiny title"> BEM VINDO À MAEZTRA </span>
              <span class="font-size-big subtitle">
                Receba em Primeira mão
              </span>
              <span class="font-size-big font-weight-bold subtitle">
                desconto e ofertas exclusivas
              </span>
              <input
                class="border-radius-medium bg-dark-white-2 border-none"
                type="text"
                placeholder="Digite seu e-mail"
              />
              <button
                class="border-radius-tiny bg-primary white border-none font-size-medium font-weight-bold"
              >
                Enviar
                <img
                  class="margin-left-8"
                  src="../assets/send-icon.svg"
                  alt="Menu"
                />
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: "Modal",
  props: {
    show: { type: Boolean, default: false },
  },
};
</script>

<style lang="scss" scoped>
.title {
  margin-top: 17.66px;
  margin-bottom: 12.71px;
}

input {
  width: 322px;
  padding: 10px 13px;
  margin-bottom: 12.5px;
  margin-top: 25.42px;
  @media (max-width: 768px) {
    width: 258px;
  }
}

button {
  width: 322px;
  padding: 10px 0px;
  @media (max-width: 768px) {
    width: 258px;
  }
}

.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: table;
  transition: opacity 0.3s ease;
}

.modal-wrapper {
  display: table-cell;
  vertical-align: middle;
}

.modal-container {
  width: 848px;
  margin: 0px auto;
  @media (max-width: 768px) {
    margin: 7px 31px;
    width: 100%;
  }
}

.margin-left-8 {
  margin-left: 8px;
}

.modal-body {
  width: 848px;
  background-color: #fff;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
  margin: 0px auto;
  transition: all 0.3s ease;
  display: flex;
  margin: 7px 0;
  @media (max-width: 768px) {
    width: 85%;
  }
}

.close {
  float: right;
  @media (max-width: 768px) {
    float: none;
    justify-content: flex-end;
    width: 85%;
  }
}

.modal-enter {
  opacity: 0;
}

.modal-leave-active {
  opacity: 0;
}

.content {
  padding-left: 50px;
  flex-direction: column;
  color: #787d83;
  @media (max-width: 768px) {
    padding: 20px;
    width: 100%;
  }
}

.modal-enter .modal-container,
.modal-leave-active .modal-container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
}

.img-modal {
  @media (max-width: 768px) {
    display: none;
  }
}

.subtitle {
  @media (max-width: 768px) {
    font-size: 16px;
  }
}
</style>
