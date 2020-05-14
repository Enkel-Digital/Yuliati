<template>
  <div>
    <v-btn
      v-for="(item, i) in items"
      :key="i"
      fab
      class="ma-2 mr-1"
      :color="color"
      :small="true"
      :href="item.link"
      target="_blank"
    >
      <v-icon dark v-text="item.icon" />
    </v-btn>
  </div>
</template>

<script>
export default {
  props: {
    large: {
      type: Boolean,
      default: false,
    },
    color: {
      type: String,
      default: "info", // Defaults to purple
    },
  },
  data: () => ({
    items: [
      {
        icon: "mdi-github-circle",
        link: "https://github.com/Icebearbear",
      },
      {
        icon: "mdi-linkedin-box",
        link: "https://www.linkedin.com/in/yuliati-yuli-70b93a1a9/",
      },
      {
        icon: "mdi-file-document-box",
        link:
          "https://docs.google.com/document/d/1TQ01z6GGq-LMY0HxDDF4_S0WEkErFGaCjdeKYU54EI0/edit?usp=sharing",
      },
      {
        icon: "mdi-email",
        link: "mailto:yuliatiyuli39@gmail.com",
      },
      {
        icon: "mdi-phone",
        link: "tel:+65 83743505",
      },
    ],
  }),
};
</script>
