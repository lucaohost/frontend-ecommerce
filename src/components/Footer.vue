<template>
  <div
    class="content display-flex justify-content-between align-items-center bg-light-black-1"
  >
    <div class="social-media margin-bottom-md-36">
      <img
        class="white margin-right-22"
        src="../assets/facebook.svg"
        alt="Logo Facebook"
      />
      <img
        class="white margin-right-22"
        src="../assets/linkedin.svg"
        alt="Logo Linkedin"
      />
      <img
        class="white margin-right-22"
        src="../assets/instagram.svg"
        alt="Logo Instagram"
      />
      <img class="white" src="../assets/youtube.svg" alt="Logo Youtube" />
    </div>
    <div class="card-flags margin-bottom-md-36">
      <img
        class="white margin-right-22"
        src="../assets/visa.svg"
        alt="Logo Visa"
      />
      <img
        class="white margin-right-22"
        src="../assets/master.svg"
        alt="Logo Master"
      />
      <img
        class="white margin-right-22"
        src="../assets/visa.svg"
        alt="Logo Visa"
      />
      <img class="white" src="../assets/master.svg" alt="Logo Master" />
    </div>
    <div class="display-flex vtex-maeztra">
      <div class="display-flex flex-column margin-right-22">
        <span class="font-size-xxtiny white margin-bottom-2"> Powered by </span>
        <img class="white" src="../assets/vtex.svg" alt="Vtex Logo" />
      </div>
      <div class="display-flex flex-column">
        <span class="font-size-xxtiny white margin-bottom-2">
          Developed by
        </span>
        <img class="white" src="../assets/maeztra.svg" alt="Maeztra Logo" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.margin-bottom-md-36 {
  @media (max-width: 768px) {
    margin-bottom: 36px;
  }
}

.margin-right-22 {
  margin-right: 22px;
}

.content {
  padding: 27px 161px;
  @media (max-width: 768px) {
    flex-direction: column;
    padding: 24px 80px;
  }
}
.flex-column {
  flex-direction: column;
}
.margin-bottom-2 {
  margin-bottom: 2px;
}
</style>
