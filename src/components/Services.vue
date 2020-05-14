<template>
  <section id="services" class="overflow-hidden">
    <v-row class="accent" no-gutters>
      <v-col class="hidden-sm-and-down" md="6">
        <v-img :src="require('@/assets/services.png')" height="100%" />
      </v-col>

      <v-col class="text-center pa-5" cols="12" md="6">
        <v-row class="fill-height" align="center" justify="center">
          <v-col cols="12">
            <base-bubble-2 style="transform: translateX(55%);" />
            <base-heading class="info--text">
              Skills and Experiences
            </base-heading>

            <base-text class="mb-5">
              What better way to learn about my Skills<br />
              Than to just see my past experiences?
            </base-text>
          </v-col>

          <v-col
            v-for="(service, i) in services"
            :key="i"
            class="text-center mb-3"
            md="6"
          >
            <v-avatar class="elevation-6 mb-2" color="#69A1BB" size="64" tile>
              <v-icon dark size="52" v-text="service.icon" />
            </v-avatar>

            <base-text>
              <div class="mb-2" v-text="service.name" />
              <div v-html="service.blurb" />
            </base-text>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </section>
</template>

<script>
export default {
  name: "Services",

  data: () => ({
    services: [
      {
        name: "Research",
        icon: "mdi-clipboard-text-outline",
        blurb: "Rolls Royce IOT department,<br />specialist researcher.",
      },

      {
        name: "Design/Architect",
        icon: "mdi-pencil-outline",
        blurb: "Database schema design<br />for Temasek Polytechnic.",
      },
      {
        name: "Frontend",
        icon: "mdi-settings-outline",
        blurb: "Data visualization dasboards<br />for various client projects.",
      },
      {
        name: "Backend",
        icon: "mdi-settings-outline",
        blurb: "Data engineering solutions<br />focused on data processing.",
      },
      {
        name: "Experienced",
        icon: "mdi-clipboard-text-outline",
        blurb: "Worked with different data<br />solutions from SQL to NoSQL.",
      },
      {
        name: "Support",
        icon: "mdi-account",
        blurb: "Great team player across<br />many teams and companies.",
      },
    ],
  }),
};
</script>
