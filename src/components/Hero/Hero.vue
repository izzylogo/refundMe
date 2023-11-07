<template>
  <main>
    <div class="hero">
      <div class="hero-sides">
        <div class="left">
            <h2>Lost your money to a scam?</h2>
            <h3>Get your money back from a scam</h3>
            <h4>Funds Recovery</h4>
        </div>
        <div class="right">
          <img :src="require('../../assets/refund.png')" alt="">
        </div>
      </div>
      <div class="hero-btn">  
          <!-- <p>If you’ve lost money to scammers, contact us now and we’ll work with you to get your money back!</p> -->
          <button>
            <router-link to="/complain">Get your money back</router-link>
          </button>
          <div class="icons">
            <div class="icon">
              <Icon icon="simple-line-icons:lock" width="18" height="18" />
              <p>FCA regulated</p>
            </div>
            <div class="icon">
              <Icon icon="game-icons:star-formation" width="18" height="18" />
              <p>UK's best-rated</p>
            </div>
            <div class="icon">
              <Icon icon="mdi:user-child-circle" width="18" height="18" />
              <p>$20m recovered</p>
            </div>
            <div class="icon">
              <Icon icon="system-uicons:user-add" width="18" height="18" />
              <p>2,000 + customers</p>
            </div>
          </div>
      </div>
      <div class="bottom">
          <img :src="require('../../assets/refund.png')" alt="">
      </div>
    </div>
  </main>
  <!-- <v-container>
    <h1>This is the home page</h1>
  </v-container> -->
</template>

<script>
import { Icon } from '@iconify/vue';
export default {
    name: 'Hero',
    components: {
		Icon,
	},

}
</script>

<style lang="scss" scoped>
@import '../../scss/Hero.scss';

</style>