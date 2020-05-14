<template>
  <section id="about" class="overflow-hidden">
    <v-row class="white" no-gutters>
      <v-col class="pa-5" cols="12" md="6">
        <base-bubble-1 style="transform: translate(5%, -5%);" />

        <base-heading class="info--text">
          About Me
        </base-heading>

        <base-text class="mb-5">
          I am passionate and keen to learn more about Data Engineering<br />
          and Big Data solutions! With experiences spanning across various<br />
          roles and companies, I am a great team player that fits right in.<br />
        </base-text>

        <br />
        <br />
        <br />

        <base-subheading class="info--text">
          Background
        </base-subheading>

        <base-text class="mb-5">
          <span>
            I studied Computer Engineering with a focus on IOT technologies,<br />
            I started getting into Big Data and data processing after<br />
            spending some time in the IOT scene where having a good data<br />
            infrastructure was of upmost importance.<br /><br />
            After my stint at Rolls Royce's IOT department, I started working<br />
            as a Data Engineer under
            <a href="https://consulting.enkeldigital.com"> Enkel Digital</a>
            consulting where I built<br />
            custom solutions for client projects.
          </span>
        </base-text>

        <br />
        <br />
        <br />

        <base-subheading class="info--text">
          Goals & Aspirations
        </base-subheading>

        <base-text class="mb-5">
          I would love to explore opportunities in the startup scene<br />
          and research institutes to work on cutting edge technologies!
        </base-text>
      </v-col>

      <v-col class="hidden-sm-and-down" md="6">
        <v-img :src="require('@/assets/aboutme.png')" height="100%" />
      </v-col>
    </v-row>
  </section>
</template>
