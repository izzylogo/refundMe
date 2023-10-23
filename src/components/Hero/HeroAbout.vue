<template>
  <div class="aboutmain">
    <div class="about">
        <h2>About Us</h2>
        <p>Our experienced team has over 20 years combined experience working in industry for banks, the Financial Conduct Authority or the Financial Ombudsman Service. </p>
        <p>We offer full transparency during the entire process and invite you to look up our registration information or to come meet us in person. The service is very straight forward and delivers results.</p>
        <p>There are tens of millions of victims every single year throughout the world. We know how to recover your funds and we helped thousands of scam victims from around the world to recover their funds.</p>
        <br>
        <div class="cofounders"
        v-if="!$vuetify.display.mdAndDown"        
        >
          <ul>
            <li>
              <div class="pics">
                <v-img 
                  class="bg-white"
                  width="300"
                  :aspect-ratio="1"
                  src='../../assets/Will.jpg'
                  cover
                  style="border-radius: 50%;"
                ></v-img>              </div>
              <div class="name"><h3>Williams Ayles</h3></div>
              <div class="position"><p>Co-Founder</p></div>
            </li>
            <li>
              <div class="pics">
                <v-img
                  class="bg-white"
                  width="300"
                  :aspect-ratio="1"
                  src='../../assets/stuart.jpg'
                  cover
                  style="border-radius: 50%;"
                ></v-img>
              </div>
              <div class="name"><h3>Stuart McFadden</h3></div>
              <div class="position"><p>Co-Founder</p></div>
            </li>
          </ul>
        </div>
        <div 
            class="small"
            v-if="$vuetify.display.mdAndDown"        
        >
            <v-carousel hide-delimiters style="height: 100%;">
                <v-carousel-item v-for="(item,i) in items" :key="i" cover>
                <div style="padding: 20px; width: 80%; margin: 0px auto">
                    <img :src="item.src" style="width: 100%" />
                    <p>{{item.name}}</p>
                    <p>Having seen how many banks were failing to support victims of scams, he set up Refundee in 2021 to help victims when they need it most.</p>
                </div>

                </v-carousel-item>
            </v-carousel>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'HeroAbout',

    data() {
      return {
        items: [
          {
            src: require('../../assets/Will.jpg'),
            name: 'Williams Ayles',
          },
          {
            src: require('../../assets/stuart.jpg'),
            name: 'Stuart McFadden',
          },
        ],
      }
    },
}
</script>

<style lang="scss" scoped>
@import "../../scss/HeroAbout.scss";
</style>