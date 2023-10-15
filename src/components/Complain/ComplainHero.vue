<template>
    <main>
        <h2>Get In Touch!</h2>
        <div class="contain">
            <div class="left">
                <h3>Online Fraud Victim?</h3>
                <h3>Leave your details to get your money back!</h3>
                <p>If you’ve been ripped off by scammers, get in touch and our team of experts will work to get your money back</p>
            </div>
            <div class="right">
                <v-form @submit.prevent>
                    <v-text-field
                        v-model="firstName"
                        :rules="rules"
                        label="Your name"
                    ></v-text-field>
                    <v-text-field
                        v-model="email"
                        :rules="rules1"
                        label="Email address"
                    ></v-text-field>
                    <v-text-field
                        v-model="scamCompany"
                        :rules="rules2"
                        label="Scam company name"
                    ></v-text-field>
                    <v-text-field
                        v-model="lastTransaction"
                        :rules="rules3"
                        label="Last transaction date"
                    ></v-text-field>
                    <v-textarea
                        v-model="story"
                        label="Tell your story"
                    ></v-textarea>
                    <v-btn type="submit" block class="mt-2">Submit</v-btn>
                </v-form>
            </div>
        </div>
    </main>
</template>

<script>
export default {
    name: 'ComplainHero',

    data: () => ({
      firstName: '',
      email: '',
      scamCompany: '',
      lastTransaction: '',
      story: '',
      rules: [
        value => {
          if (value) return true

          return 'You must enter a first name.'
        },
      ],
      rules1: [
        value => {
          if (value) return true

          return 'You must enter an email.'
        },
      ],
      rules2: [
        value => {
          if (value) return true

          return 'You must enter the name of the scam company.'
        },
      ],
      rules3: [
        value => {
          if (value) return true

          return 'You must enter when you made a last transaction.'
        },
      ],
      rules4: [
        value => {
          if (value) return true

          return 'You can enter a story.'
        },
      ],
    }),
}
</script>

<style lang="scss" scoped>
@import '../../scss/ComplainHero.scss';
</style>