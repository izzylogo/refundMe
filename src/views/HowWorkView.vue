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
            <v-expansion-panels variant="accordion">
            <v-expansion-panel
                style="background-color: transparent; border-top: 1px solid black; border-bottom:  1px solid black;"
            >
            <v-expansion-panel-title>
                <p>The <span>3</span> stages</p>
            </v-expansion-panel-title>
            <v-expansion-panel-text>
                <ol>
                    <li>
                        <h3>The Investigation</h3>
                        <p>Our Fraud Investigators will assess your case to if we can help.</p>
                    </li>
                    <li>
                        <h3>The Bank</h3>
                        <p>Refundee will prepare your individual case and submit a bespoke report to the bank in order to receive their formal response. </p>
                    </li>
                    <li>
                        <h3>The Financial Ombudsman Service (FOS)</h3>
                        <p>If the bank won't reimburse you, Refundee will present your case to the FOS who will conduct an independent review. This is the final stage; it determines the amount that you will be refunded.</p>
                    </li>
                </ol>
            </v-expansion-panel-text>
            </v-expansion-panel>
            <v-expansion-panel
                style="background-color: transparent; border-top: 1px solid black; border-bottom:  1px solid black;"
            >
            <v-expansion-panel-title>
                <p>Fees</p>
            </v-expansion-panel-title>
            <v-expansion-panel-text>
                <p>If we’re successful we charge 15% plus VAT on the money you get back.</p>
            </v-expansion-panel-text>
            </v-expansion-panel>
            <v-expansion-panel
                style="background-color: transparent; border-top: 1px solid black; border-bottom:  1px solid black;"
            >
            <v-expansion-panel-title>
                <p>Do it yourself</p>
            </v-expansion-panel-title>
            <v-expansion-panel-text>
                <p>You don’t need to use a Claims Management Company like Refundee to get your money back (and can save paying a fee if you don’t). If you feel confident doing it yourself, you can.</p>
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