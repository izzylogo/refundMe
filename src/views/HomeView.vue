<template>
  <div class="cover">
    <main>
      <Hero/>
      <HeroAbout/>
      <Why/>
      <Types/>
    </main>
  </div>
</template>

<script>
import Hero from '@/components/Hero/Hero.vue';
import HeroAbout from '@/components/Hero/HeroAbout.vue';
import Why from '@/components/Hero/Why.vue';
import Types from '@/components/Hero/Types.vue';
export default{
  name: 'HomeView',
  components: {Hero, HeroAbout, Why, Types,}
};
</script>

<style lang="scss" scoped>

main{
  overflow-x: hidden;
  overflow-y: auto;
  max-width: 1400px;
  margin: 0px auto;
  
  /* font-family: Inter, Verdana, sans-serif; */

  &::-webkit-scrollbar-track {
        background-color: transparent;
      }
      &::-webkit-scrollbar {
        width: 5px;
      }
      &::-webkit-scrollbar-thumb {
        background-color: red;
        -moz-border-radius: 4px;
        -webkit-border-radius: 4px;
        border-radius: 4px;
        -moz-border-radius: 4px;
        -webkit-border-radius: 4px;
        border-radius: 4px;
      }

}
.cover{
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
        background-color: red;
        -moz-border-radius: 4px;
        -webkit-border-radius: 4px;
        border-radius: 4px;
        -moz-border-radius: 4px;
        -webkit-border-radius: 4px;
        border-radius: 4px;
      }

}
</style>
