<template>
  <div
    :class="$vuetify.breakpoint.mdAndUp ? 'text-right' : 'text-center'"
  >
    <v-form
      ref="form"
      v-model="valid"
      lazy-validation
    >
      <base-info-card
        :title="title"
        :subtitle="subtitle"
        space="4"
        color="primary"
      />

      <base-text-field
        id="frmNameA"
        v-model="name"
        label="Name"
        :rules="nameRules"
        validate-on-blur
        name="name"
        required
        autocomplete="name"
        class="contactForm"
      />

      <base-text-field
        id="frmEmailA"
        v-model="email"
        label="Email"
        :rules="emailRules"
        validate-on-blur
        type="email"
        name="email"
        required
        autocomplete="email"
        class="contactForm"
      />

      <base-text-field
        v-model="subject"
        label="Subject"
        :rules="subjectRules"
        validate-on-blur
      />

      <base-textarea
        v-model="text"
        class="mb-0"
        label="Your Need & Description"
        :rules="textRules"
        validate-on-blur
      />

      <v-btn
        outlined
        x-large
        class="rounded mb-5 mx-auto"
        @click="save_email"
      >
        Send message
      </v-btn>
      <div
        class="primaryText mb-5 smallText"
      >
        This site is protected by reCAPTCHA and the Google
        <a href="https://policies.google.com/privacy">Privacy Policy</a> and
        <a href="https://policies.google.com/terms">Terms of Service</a> apply.
      </div>
      <octo-email-saved
        ref="dialog01"
        timeout="3000"
        text="Email sent!"
      />
    </v-form>
  </div>
</template>

<script>
  export default {
    name: 'BaseContactForm',

    props: {
      subtitle: String,
      title: {
        type: String,
        default: 'MAIL US YOUR MESSAGE',
      },
    },

    data: () => ({
      valid: true,
      name: '',
      email: '',
      subject: '',
      text: '',
      emailRules: [
        v => /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{1,10})+$/.test(v) || 'E-mail must be valid',
      ],
      textRules: [
        v => !!v || 'Missing text body',
      ],
      nameRules: [
        v => !!v || 'Missing name',
      ],
      subjectRules: [
        v => !!v || 'Missing subject',
      ],
    }),
    methods: {
      test_email (mail) {
        const re = /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{1,10})+$/
        return re.test(mail)
      },
      are_all_fields_filled () {
        return this.name !== '' && this.email !== '' && this.subject !== '' && this.text !== ''
      },
      async save_email () {
        this.validate()
        const token = await this.recaptcha()
        if (this.test_email(this.email) && this.are_all_fields_filled()) {
          let adress = 'https://us-central1-octomancer-website.cloudfunctions.net/sendUsEmail'
          adress += '?name=' + this.name
          adress += '&email=' + this.email
          adress += '&subject=' + this.subject
          adress += '&text=' + this.text
          adress += '&token=' + token
          this.axios(
            {
              method: 'post',
              url: adress,
              data: {
              },
              headers: { 'Access-Control-Allow-Origin': '*' },
            },
          ).catch()
          this.name = ''
          this.email = ''
          this.subject = ''
          this.text = ''
          this.$refs.dialog01.openDialog()
        }
      },
      validate () {
        this.$refs.form.validate()
      },
      reset () {
        this.$refs.form.reset()
      },
      resetValidation () {
        this.$refs.form.resetValidation()
      },
      async recaptcha () {
        // (optional) Wait until recaptcha has been loaded.
        await this.$recaptchaLoaded()

        // Execute reCAPTCHA with action "login".
        return await this.$recaptcha('login')
        // Do stuff with the received token.
      },
    },

    // Injected from the Vuetify Themeable mixin
    inject: ['theme'],
  }
</script>

<style scoped>
.contactForm :-webkit-autofill,
input:-webkit-autofill:hover,
input:-webkit-autofill:focus,
textarea:-webkit-autofill,
textarea:-webkit-autofill:hover,
textarea:-webkit-autofill:focus,
select:-webkit-autofill,
select:-webkit-autofill:hover,
select:-webkit-autofill:focus {
  -webkit-box-shadow: 0 0 0px 1000px #031c28 inset !important;
  transition: all 10000s ease-in-out 0s;
  -webkit-text-fill-color: white;
}
.smallText {
  font-size: 0.7rem !important;
}
</style>
