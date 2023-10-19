<template>
    <main>
        <div class="top">
            <h1>How the process works</h1>
            <p>There are three stages</p>
        </div>
        <div class="process">
            <div class="card">
                <img :src="require('../assets/business_chat.svg')" alt="">
                <h4>Contact us for free case review</h4>
                <p>Our team of experts will assess your case and identify which kind of fraud had been done and whether money can be recovered or not. The case review is free so you can stop Hesitating and contact us right away.</p>
            </div>
            <img :src="require('../assets/long-pointer.svg')" class="arr" alt="">
            <div class="card">
                <img :src="require('../assets/text_files.svg')" alt="">
                <h4>Contact us for free case review</h4>
                <p>Our team of experts will assess your case and identify which kind of fraud had been done and whether money can be recovered or not. The case review is free so you can stop Hesitating and contact us right away.</p>
            </div>
            <img :src="require('../assets/long-pointer.svg')" class="arr" alt="">
            <div class="card">
                <img :src="require('../assets/order_confirmed.svg')" alt="">
                <h4>Contact us for free case review</h4>
                <p>Our team of experts will assess your case and identify which kind of fraud had been done and whether money can be recovered or not. The case review is free so you can stop Hesitating and contact us right away.</p>
            </div>
        </div>
        <div class="talk">
            <p>If successful, you receive the money back into your account!</p>
            <p>We then arrange our invoice. Of course, we keep you updated throughout so that you know what's happening. We handle everything to keep it as easy for you as possible.</p>
            <br>
            <p>If unsuccessful, you won’t pay a penny.</p>
        </div>
        <div class="ask">
            <v-expansion-panels style="box-shadow: none;" variant="accordion">
            <v-expansion-panel
                style="
                background-color: transparent; 
                border-top: 1px solid black; 
                border-bottom:  1px solid black;
                box-shadow: none;
                "
                v-for="i in 3"
                :key="i"
            >
            <v-expansion-panel-title style="box-shadow: none;">
                <h2>Israel</h2>
            </v-expansion-panel-title>
            <v-expansion-panel-text style="box-shadow: none;">
                <p>Meeeee</p>
            </v-expansion-panel-text>
            </v-expansion-panel>
            </v-expansion-panels>
        </div>
        <br>
        <br>
        <button class="redirect">
            <router-link to="/complain">Get Your Money</router-link>
        </button>
        <br>
        <br>
    </main>
</template>

<style lang="scss" scoped>
@import '../scss/HowWork.scss';
</style>