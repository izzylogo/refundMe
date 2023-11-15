<template>
    <div class="testimonals">
        <div class="testimonal-cover">
            <h2>Testimonials</h2>
            <div 
            class="small"
            >
            <v-sheet
                class="mx-auto"
                max-width="100%"
            >
                <v-slide-group
                show-arrows
                >
                <v-slide-group-item
                    v-for="test in testimonal"
                    style="gap: 20px;"
                    :key="test"
                >
                    <v-card
                        class="ma-4"
                        color='#e9f2f7'    
                    >
                        <v-card-text>
                            <div class="thumbnail">
                                <img :src="test.image" alt="image">
                            </div>
                        </v-card-text>
                        <v-card-text>
                            <p>{{ test.text }}</p>
                        </v-card-text>
                    </v-card>
                    <!-- <v-btn
                    class="ma-2"
                    rounded
                    :color="isSelected ? 'primary' : undefined"
                    @click="toggle"
                    >
                    Options {{ n }}
                    </v-btn> -->
                </v-slide-group-item>
                </v-slide-group>
            </v-sheet>
        </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Testimonal',

    data() {
      return {
        testimonal: [
          {
            image: require('../../assets/testimonal1 (1).jpg'),
            text: `After falling victim to a Bitcoin scam, I found myself in a desperate situation. The scammer disappeared, and the police were of little help, but then I discovered RefundTrace. Their expertise in exploiting scammers' vulnerabilities and understanding of the Blockchain resulted in the successful recovery of my funds. In a world where government assistance often falls short, RefundTrace proved to be reliable.`
          },
          {
            image: require('../../assets/testimonal1 (2).jpg'),
            text: `While initially sceptical of platforms claiming to recover lost money, the guys at RefundTrace exceeded my expectations. Their diligent efforts, tracing, and retrieving a considerable sum lost to a  fraud I fell for, showcased a high level of professionalism. For anyone grappling with the repercussions of scams, I recommend RefundTrace.`
          },
          {
            image: require('../../assets/testimonal1 (3).jpg'),
            text: ` Their remarkable prowess was evident as they successfully recovered $63,000 worth of Ethereum. RefundTrace is unequivocally my go-to option for those who have been thrown into the deep end of a financial fraud situation.`
          },
          {
            image: require('../../assets/testimonal1 (4).jpg'),
            text: ` I got done for 80k pounds because someone somehow got into my crypto wallet. And I turned to RefundTrace. They have recovered 60k so far and are tracking the reset. If you're in a similar situation, RefundTrace is a solid choice`
          },
          {
            image: require('../../assets/testimonal1 (5).jpg'),
            text: `I lost a significant amount of money to a scam and was at my wit's end. I had almost given up hope of ever seeing my money again when I found the guys at RefundTrace. They were able to recover my funds and even went the extra mile to help me secure my accounts against future scams. I am incredibly grateful for their expertise and dedication.`
          },
          {
            image: require('../../assets/testimonal1 (6).jpg'),
            text: ` I was at first hesitant to seek professional help for recovering my lost cryptocurrency, as I feared the cost and complexity of the process. However, after consulting with Will and Stuart, I realized that their expertise and experience were worth the investment. They were able to recover my funds quickly and efficiently, and their communication was clear and consistent throughout the process.`
          },
        ],
      }
    },
}
</script>

<style lang="scss" scoped>
@import '../../scss/Testimonal.scss';
</style>