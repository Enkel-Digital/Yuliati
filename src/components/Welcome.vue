<template>
  <section id="welcome" class="overflow-hidden">
    <v-row no-gutters>
      <v-col class="hidden-sm-and-down" md="6">
        <v-img :src="require('@/assets/welcome.png')" height="100vh" />
      </v-col>

      <v-col
        class="align-content-space-between layout wrap"
        cols="12"
        md="6"
        :pa-5="$vuetify.breakpoint.smAndDown"
      >
        <base-bubble-1 style="transform: rotate(180deg) translateY(25%);" />

        <!-- Add space for mobile to stay below the floating icons -->
        <br />
        <br />

        <v-row align="center" justify="center">
          <v-col cols="10" md="6">
            <base-heading>Welcome!</base-heading>
            <base-text>
              Hello! I am Yuliati and you are looking at my portfolio website!
              Okay first, who the hell am I? Well, as my friends would describe
              me, I am someone with an uncanny personality but honestly I think
              I am more playful and annoying by their standards 😁<br /><br />
              I am super adventurous and I believe that in life, you have
              NOTHING TO LOSE and I am super driven to make my dreams come true.
            </base-text>

            <!-- Go to next section on click -->
            <base-btn href="#recent-projects" class="mt-4">
              Learn More!
            </base-btn>

            <base-bubble-2
              style="transform: rotate(180deg) translate(-200px, -15%);"
            />

            <br />
            <br />
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </section>
</template>
