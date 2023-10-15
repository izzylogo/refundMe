<template>
  <main>
    <div class="hero">
        <div class="left">
            <h2>Lost your money to a scam?</h2>
            <h3>Get your money back from a scam</h3>
            <h4>Funds Recovery</h4>
            <div class="left-btn">
                <p>If you’ve lost money to scammers, contact us now and we’ll work with you to get your money back!</p>
                <button>
                  <router-link to="/about">know more about us?</router-link>
                </button>
            </div>
        </div>
        <!-- <div class="right"></div> -->
    </div>
  </main>
  <!-- <v-container>
    <h1>This is the home page</h1>
  </v-container> -->
</template>

<script>
export default {
    name: 'Hero',

}
</script>

<style lang="scss" scoped>
@import '../../scss/Hero.scss';

</style>