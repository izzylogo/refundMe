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
                <v-form @submit.prevent="sendMessage">
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
                        v-model="amountLost"
                        :rules="rules5"
                        label="Amount Lost"
                    ></v-text-field>
                    <v-text-field
                        v-model="currency "
                        :rules="rules6"
                        label="Currency"
                    ></v-text-field>
                    <v-textarea
                        v-model="story"
                        label="Tell your story"
                        :rules="rules4"
                    ></v-textarea>
                   
                    <v-select
                    label="Country"
                    :items="states"
                    variant="outlined"
                    v-model="thelocation"
                  ></v-select>
                    <v-btn type="submit" :loading="this.loading" block class="mt-2">Submit</v-btn>
                </v-form>
            </div>
        </div>
    </main>
</template>

<script>
import axios from 'axios'
export default {
    name: 'ComplainHero',
    data: () => ({
      firstName: '',
      email: '',
      scamCompany: '',
      lastTransaction: '',
      amountLost: '',
      currency: '',
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
      rules5: [
        value => {
          if (value) return true

          return 'You can enter a story.'
        },
      ],
      rules6: [
        value => {
          if (value) return true

          return 'You can enter a story.'
        },
      ],
      thelocation: "",
      manager: "",
      loading: false,
      states: [
      "Afghanistan",
      "Albania",
      "Algeria",
      "Andorra",
      "Angola",
      "Antigua and Barbuda",
      "Argentina",
      "Armenia",
      "Australia",
      "Austria",
      "Azerbaijan",
      "Bahamas",
      "Bahrain",
      "Bangladesh",
      "Barbados",
      "Belarus",
      "Belgium",
      "Belize",
      "Benin",
      "Bhutan",
      "Bolivia",
      "Bosnia and Herzegovina",
      "Botswana",
      "Brazil",
      "Brunei",
      "Bulgaria",
      "Burkina Faso",
      "Burundi",
      "Côte d'Ivoire",
      "Cabo Verde",
      "Cambodia",
      "Cameroon",
      "Canada",
      "Central African Republic",
      "Chad",
      "Chile",
      "China",
      "Colombia",
      "Comoros",
      "Congo (Congo-Brazzaville)",
      "Costa Rica",
      "Croatia",
      "Cuba",
      "Cyprus",
      "Czechia",
      "Democratic Republic of the Congo (Congo-Kinshasa)",
      "Denmark",
      "Djibouti",
      "Dominica",
      "Dominican Republic",
      "Ecuador",
      "Egypt",
      "El Salvador",
      "Equatorial Guinea",
      "Eritrea",
      "Estonia",
      "Eswatini",
      "Ethiopia",
      "Fiji",
      "Finland",
      "France",
      "Gabon",
      "Gambia",
      "Georgia",
      "Germany",
      "Ghana",
      "Greece",
      "Grenada",
      "Guatemala",
      "Guinea",
      "Guinea-Bissau",
      "Guyana",
      "Haiti",
      "Holy See",
      "Honduras",
      "Hungary",
      "Iceland",
      "India",
      "Indonesia",
      "Iran",
      "Iraq",
      "Ireland",
      "Israel",
      "Italy",
      "Jamaica",
      "Japan",
      "Jordan",
      "Kazakhstan",
      "Kenya",
      "Kiribati",
      "Kuwait",
      "Kyrgyzstan",
      "Laos",
      "Latvia",
      "Lebanon",
      "Lesotho",
      "Liberia",
      "Libya",
      "Liechtenstein",
      "Lithuania",
      "Luxembourg",
      "Madagascar",
      "Malawi",
      "Malaysia",
      "Maldives",
      "Mali",
      "Malta",
      "Marshall Islands",
      "Mauritania",
      "Mauritius",
      "Mexico",
      "Micronesia",
      "Moldova",
      "Monaco",
      "Mongolia",
      "Montenegro",
      "Morocco",
      "Mozambique",
      "Myanmar (formerly Burma)",
      "Namibia",
      "Nauru",
      "Nepal",
      "Netherlands",
      "New Zealand",
      "Nicaragua",
      "Niger",
      "Nigeria",
      "North Macedonia",
      "Norway",
      "Oman",
      "Pakistan",
      "Palau",
      "Palestine State",
      "Panama",
      "Papua New Guinea",
      "Paraguay",
      "Peru",
      "Philippines",
      "Poland",
      "Portugal",
      "Qatar",
      "Romania",
      "Russia",
      "Rwanda",
      "Saint Kitts and Nevis",
      "Saint Lucia",
      "Saint Vincent and the Grenadines",
      "Samoa",
      "San Marino",
      "Sao Tome and Principe",
      "Saudi Arabia",
      "Senegal",
      "Serbia",
      "Seychelles",
      "Sierra Leone",
      "Singapore",
      "Slovakia",
      "Slovenia",
      "Solomon Islands",
      "Somalia",
      "South Africa",
      "South Korea",
      "South Sudan",
      "Spain",
      "Sri Lanka",
      "Sudan",
      "Suriname",
      "Sweden",
      "Switzerland",
      "Syria",
      "Tajikistan",
      "Tanzania",
      "Thailand",
      "Timor-Leste",
      "Togo",
      "Tonga",
      "Trinidad and Tobago",
      "Tunisia",
      "Turkey",
      "Turkmenistan",
      "Tuvalu",
      "Uganda",
      "Ukraine",
      "United Arab Emirates",
      "United Kingdom",
      "United States of America",
      "Uruguay",
      "Uzbekistan",
      "Vanuatu",
      "Venezuela",
      "Vietnam",
      "Yemen",
      "Zambia",
      "Zimbabwe",
      ],
      baseUrl: 'https://gmx-v3nl.onrender.com/refundtrace',
      responseData: null
    }),
    methods: {
      getDetail(){
        console.log(this.firstName, this.email, this.scamCompany, this.lastTransaction, this.amountLost, this.currency, this.story, this.thelocation)
      },
      async sendMessage() {
        try {
          this.loading = true
          const reponse = await axios.post('https://gmx-v3nl.onrender.com/refundtrace'  , {
            name: this.firstName,
            email: this.email,
            cname: this.scamCompany,
            tdate: this.lastTransaction,
            amount: this.amountLost,
            currency: this.currency,
            story: this.story,
            location: this.thelocation,
          })
          this.reponseData = reponse.data
          this.loading = false
          console.log('Successful')
        } catch (error) {
          console.log('Error', error);
        }
      },
    }
}
</script>

<style lang="scss" scoped>
@import '../../scss/ComplainHero.scss';
</style>