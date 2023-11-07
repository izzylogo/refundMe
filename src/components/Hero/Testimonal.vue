<template>
    <div class="testimonals">
        <div class="testimonal-cover">
            <div 
            class="small"
        >
            <!-- <v-carousel hide-delimiters style="height: 100%;">
                <v-carousel-item v-for="(item,i) in items" :key="i" cover>
                    <v-card>
                        hello
                    </v-card>
                <div style="padding: 20px; width: 80%; margin: 0px auto">
                    <p>{{item.name}}</p>
                    <p>Having seen how many banks were failing to support victims of scams, he set up Refundee in 2021 to help victims when they need it most.</p>
                </div>

                </v-carousel-item>
            </v-carousel> -->
            <v-sheet
                class="mx-auto"
                max-width="100%"
            >
                <v-slide-group
                show-arrows
                >
                <v-slide-group-item
                    v-for="n in 6"
                    style="gap: 20px;"
                    :key="n"
                >
                    <v-card class="ma-4">
                        <v-card-text>
                            <h2>johhna hancock-blake</h2>
                            <h5>realtor</h5>
                        </v-card-text>
                        <v-card-text>
                            <p>Being a high-strung person, i have to admit johnna immediately picked up on my personality type and provided me a Client Experience tailored to me and my expectations. She is very good at what she does. </p>
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
@import '../../scss/Testimonal.scss';
</style>