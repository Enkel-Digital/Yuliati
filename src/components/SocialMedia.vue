<template>
  <div>
    <v-btn
      v-for="(item, i) in items"
      :key="i"
      fab
      class="ma-2"
      color="info"
      :small="true"
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
  },
  data: () => ({
    items: [
      {
        icon: "mdi-github-circle",
      },
      {
        icon: "mdi-linkedin-box",
      },
      {
        icon: "mdi-email",
      },
      {
        icon: "mdi-phone",
      },
    ],
  }),
};
</script>
