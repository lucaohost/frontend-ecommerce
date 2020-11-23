<template>
  <div class="black">
    <span class="font-size-xbig font-weight-bold">
      {{ title }}
    </span>
    <p class="font-size-normal">{{ text }}</p>
  </div>
</template>

<script>
export default {
  name: "TitleWithText",
  data() {
    return {
      title: "Lorem ipsum",
      text:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Interdum mauris posuere fusce proin mattis. Hendrerit cras ut nunc enim dictum. Mattis proin ut quis donec sed eget nulla. Vel mi ut mauris integer. Nibh sagittis in lobortis sed cursus condimentum velit pharetra. Amet luctus ut vulputate scelerisque placerat consequat. Neque arcu mi iaculis id. Vel vitae, pharetra, a nec tristique. Feugiat id tortor eu mauris pulvinar velit massa. Ut ornare augue eget convallis volutpat aliquet. Sed sed pellentesque porttitor phasellus donec condimentum sit sapien.",
    };
  },
};
</script>
