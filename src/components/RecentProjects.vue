<template>
  <section id="recent-projects" class="overflow-hidden">
    <v-row no-gutters>
      <v-col class="primary text-center pa-5 white--text" cols="12" md="6">
        <base-bubble-1 style="transform: rotate(180deg) translateX(25%);" />

        <base-heading>
          Recent Projects
        </base-heading>

        <base-text class="mb-5" style="font-weight: 200;">
          *Click to learn more.
        </base-text>

        <br />

        <v-card color="secondary">
          <v-container class="pa-2">
            <v-row>
              <v-col v-for="(project, i) in projects" :key="i" cols="12" md="6">
                <a :href="project.link" target="_blank">
                  <v-img
                    :src="require(`@/assets/${project.image}.jpeg`)"
                    max-height="300"
                  />
                </a>
              </v-col>
            </v-row>
          </v-container>
        </v-card>
      </v-col>

      <v-col class="hidden-sm-and-down" md="6">
        <v-img :src="require('@/assets/recentprojects.png')" height="100%" />
      </v-col>
    </v-row>
  </section>
</template>

<script>
export default {
  name: "RecentProjects",
  data: () => ({
    projects: [
      {
        image: "project1",
        link: "https://github.com/Enkel-Digital/",
      },
      {
        image: "project2",
        link: "https://github.com/icecreamforfree/robot-cone",
      },
      {
        image: "project3",
        link: "https://github.com/icecreamforfree/robot-aglioolio/",
      },
      {
        image: "project4",
        link: "https://github.com/Enkel-Digital/class-express-app",
      },
    ],
  }),
};
</script>
