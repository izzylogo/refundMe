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
                    <v-text-field
                        v-model="lastTransaction"
                        :rules="rules3"
                        label="Amount Lost"
                    ></v-text-field>
                    <v-text-field
                        v-model="lastTransaction"
                        :rules="rules3"
                        label="Currency"
                    ></v-text-field>
                    <v-textarea
                        v-model="story"
                        label="Tell your story"
                    ></v-textarea>
                    <v-select
                      v-model="select"
                      :items="states"
                      density="compact"
                      variant="outlined"
                      label="Location name"
                      class="mb-2"
                      required
                    ></v-select>
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
      thelocation: "",
      manager: "",
      states: [
        "Alabama",
        "Alaska",
        "American Samoa",
        "Arizona",
        "Arkansas",
        "California",
        "Colorado",
        "Connecticut",
        "Delaware",
        "District of Columbia",
        "Federated States of Micronesia",
        "Florida",
        "Georgia",
        "Guam",
        "Hawaii",
        "Idaho",
        "Illinois",
        "Indiana",
        "Iowa",
        "Kansas",
        "Kentucky",
        "Louisiana",
        "Maine",
        "Marshall Islands",
        "Maryland",
        "Massachusetts",
        "Michigan",
        "Minnesota",
        "Mississippi",
        "Missouri",
        "Montana",
        "Nebraska",
        "Nevada",
        "New Hampshire",
        "New Jersey",
        "New Mexico",
        "New York",
        "North Carolina",
        "North Dakota",
        "Northern Mariana Islands",
        "Ohio",
        "Oklahoma",
        "Oregon",
        "Palau",
        "Pennsylvania",
        "Puerto Rico",
        "Rhode Island",
        "South Carolina",
        "South Dakota",
        "Tennessee",
        "Texas",
        "Utah",
        "Vermont",
        "Virgin Island",
        "Virginia",
        "Washington",
        "West Virginia",
        "Wisconsin",
        "Wyoming",
      ],
    }),
}
</script>

<style lang="scss" scoped>
@import '../../scss/ComplainHero.scss';
</style>