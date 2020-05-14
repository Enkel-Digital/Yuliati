<template>
  <section id="get-in-touch" class="overflow-hidden">
    <v-row class="info white--text" no-gutters>
      <v-col class="hidden-sm-and-down" md="6">
        <v-img :src="require('@/assets/contact.png')" height="100%" />
      </v-col>

      <v-col class="pa-5" cols="12" md="6">
        <base-bubble-1 />

        <base-heading class="mb-5">
          Get In Touch
        </base-heading>

        <SocialMedia color="white" />

        <br />

        <v-sheet color="transparent" max-width="600">
          <v-text-field v-model="name" color="info" label="Name" solo flat />

          <v-text-field v-model="email" color="info" label="Email" solo flat />

          <v-text-field
            v-model="subject"
            color="info"
            label="Subject"
            solo
            flat
          />

          <v-textarea
            v-model="message"
            color="info"
            label="Message"
            solo
            flat
          />

          <base-btn @click="submit">Send</base-btn>
        </v-sheet>
      </v-col>
    </v-row>
  </section>
</template>

<script>
export default {
  name: "GetInTouch",
  components: {
    SocialMedia: () => import("@/components/SocialMedia"),
  },
  data() {
    return {
      name: "",
      email: "",
      subject: "",
      message: "",
    };
  },
  methods: {
    submit() {
      const form = {
        name: this.name,
        email: this.email,
        subject: this.subject,
        message: this.message,
        // "g-recaptcha-response": grecaptcha.getResponse(), // Get the response token from the captcha UI
      };

      // If neither name is given, or email is not given
      // Alert and Break out of the function
      if (!form.name || !form.email)
        return alert("Please at least fill in your name, and provide a email!");

      // Save detail and send emails out
      fetch(
        "https://us-central1-ekd-landing-page.cloudfunctions.net/yuliGetInTouch-yuliGetInTouch",
        {
          method: "POST",
          mode: "no-cors",
          cache: "no-cache",
          headers: {
            "Content-Type": "application/json",
          },
          body: JSON.stringify(form),
        }
      )
        .then((response) => {
          console.log(response);
          alert("Contact form submitted, I will reply asap. Thank you!");
        })
        .catch((error) => {
          console.error(error);
          alert(
            "Hey there! So sorry but it seems like that failed. Please do email directly instead!"
          );
        });
    },
    // captchaError(error) {
    //   console.log("Captcha error: ", error);
    //   alert(
    //     "Captcha error encounted! Cannot submit form for now. Please try reloading the page."
    //   );
    // },
  },
};
</script>
