<template>
  <div class="cover">
    <!-- <main> -->
      <Hero/>
      <HeroAbout/>
      <HeroHow/>
      <Types/>
      <Why/>
      <Testimonal/>
    <!-- </main> -->
  </div>
</template>

<script>
import Hero from '@/components/Hero/Hero.vue';
import HeroAbout from '@/components/Hero/HeroAbout.vue';
import Why from '@/components/Hero/Why.vue';
import Types from '@/components/Hero/Types.vue';
import HeroHow from '@/components/Hero/HeroHow.vue';
import Testimonal from '@/components/Hero/Testimonal.vue';
export default{
  name: 'HomeView',
  components: {Hero, HeroAbout, Why, Types, HeroHow, Testimonal,}
};
</script>

<style lang="scss" scoped>

/* main{
  overflow-x: hidden;
  overflow-y: auto;
  max-width: 1400px;
  margin: 0px auto;
  
  &::-webkit-scrollbar-track {
        background-color: transparent;
      }
      &::-webkit-scrollbar {
        width: 5px;
      }
      &::-webkit-scrollbar-thumb {
        background-color: rgb(0, 255, 229);
        -moz-border-radius: 4px;
        -webkit-border-radius: 4px;
        border-radius: 4px;
        -moz-border-radius: 4px;
        -webkit-border-radius: 4px;
        border-radius: 4px;
      }

} */
.cover{
  display: flex;
  flex-direction: column;
  overflow-x: hidden;
  overflow-y: auto;
  /* font-family: Inter, Verdana, sans-serif; */

  &::-webkit-scrollbar-track {
        background-color: transparent;
      }
      &::-webkit-scrollbar {
        width: 5px;
      }
      &::-webkit-scrollbar-thumb {
        background-color: rgb(0, 106, 255);
        -moz-border-radius: 4px;
        -webkit-border-radius: 4px;
        border-radius: 4px;
        -moz-border-radius: 4px;
        -webkit-border-radius: 4px;
        border-radius: 4px;
      }

}
</style>
