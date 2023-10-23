<template>
    <div class="aboutmain">
        <div class="about-top">
            <h1>About ReundMe and the team</h1>
            <p>You will only work with experts when you deal with Refundee</p>
        </div>
        <div class="founder">
            <h2>Our Founders</h2>
            <div 
                class="founders"
                v-if="!$vuetify.display.mdAndDown"    
            >
                <ul>
                    <li>
                        <img :src="require('../../assets/Will.jpg')" alt="">
                        <div class="detail">
                            <h3>Williams Ayles</h3>
                            <div class="text">
                                <p>Will’s background in financial services started in multi asset investment analysis before moving to Monzo Bank. His specialism in Operations meant that he’s worked across a number of different areas including Lending, Vulnerable Customer, and Financial Difficulties. He then led the Business Banking Operations at Monzo.</p>
                                <p>Having seen how many banks were failing to support victims of scams, he set up Refundee in 2021 to help victims when they need it most.</p>
                            </div>
                        </div>
                    </li>
                    <li>
                        <img :src="require('../../assets/stuart.jpg')" alt="">
                        <div class="detail">
                            <h3>Stuart McFadden</h3>
                            <div class="text">
                                <p>Will’s background in financial services started in multi asset investment analysis before moving to Monzo Bank. His specialism in Operations meant that he’s worked across a number of different areas including Lending, Vulnerable Customer, and Financial Difficulties. He then led the Business Banking Operations at Monzo.</p>
                                <p>Having seen how many banks were failing to support victims of scams, he set up Refundee in 2021 to help victims when they need it most.</p>
                            </div>
                        </div>
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
        <div class="about-det">
            <h4>What We Do?</h4>
            <p>We can track and expose scammers and refund your money.  We handle Binary Scams, Fake Initial Coin Offerings (ICOs), CFD Trading Scams to Crypto Trading Scams, and more. So if you fall in any of these categories, do not fret. We have got you covered.</p>
            <p>Our experts use digital tools, machine learning algorithms, and automatic threat detection systems. The Global Payback also provides a groundbreaking BI algorithm. This AI-assisted algorithm provides informative reports for individuals and corporations seeking to acquire business information cost-effectively and immediately.</p>
            <p>Unfortunately, the general public is not aware of how massive and prevalent the world of scams has become. We are sad to report that tens of millions of people lose their money to fraud every year. If you or your loved ones have had the misfortune of falling prey to financial fraud, there is a course of action you can take.</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AboutHero',

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
@import '../../scss/AboutHero.scss';

</style>