<template>
  <div class="herohow">
    <div class="cover">
        <div class="left">
            <h2>How it works</h2>
            <button>
                <router-link to="/how-works">How it Works</router-link>
            </button>
        </div>
        <div class="right">
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
                        <p>RefundTrace will prepare your individual case and submit a bespoke report to the bank in order to receive their formal response. </p>
                    </li>
                    <li>
                        <h3>The Financial Ombudsman Service (FOS)</h3>
                        <p>If the bank won't reimburse you, RefundTrace will present your case to the FOS who will conduct an independent review. This is the final stage; it determines the amount that you will be refunded.</p>
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
                <p>You don’t need to use a Claims Management Company like RefundTrace to get your money back (and can save paying a fee if you don’t). If you feel confident doing it yourself, you can.</p>
            </v-expansion-panel-text>
            </v-expansion-panel>
            </v-expansion-panels>
        </div>
        <div class="bottom">
            <button>
                <router-link to="/how-works">How it Works</router-link>
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