<template>
  <div class="herohow">
    <div class="cover">
        <div class="left">
            <h2>How it works</h2>
            <button>
                <router-link to="/how-work">How it Works</router-link>
            </button>
        </div>
        <div class="right">
            <v-expansion-panels variant="accordion">
            <v-expansion-panel
                style="background-color: transparent; border-top: 1px solid black; border-bottom:  1px solid black;"
                v-for="i in 3"
                :key="i"
            >
            <v-expansion-panel-title>
                <p>Israel</p>
            </v-expansion-panel-title>
            <v-expansion-panel-text>
                <p>Meeeee</p>
            </v-expansion-panel-text>
            </v-expansion-panel>
            </v-expansion-panels>
        </div>
        <div class="bottom">
            <button>
                <router-link to="/how-work">How it Works</router-link>
            </button>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name: "HeroHow"

}
</script>

<style lang="scss" scoped>
@import "../../scss/HeroHow.scss";
</style>