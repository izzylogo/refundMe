<template>
  <main>
    <div class="types-contain">
        <h2>Types Of Scams</h2>
        <div class="card-cover">
            <div class="cards" v-for="scam in types" :key="scam.name" >
                <img :src='scam.img' alt="banking scams">
                <p>{{scam.name}}</p>
            </div>
        </div>
    </div>
  </main>
</template>

<script>
export default {
    name: 'Types',

    data() {
        return{
            types: [
                    {
                        img: require("../../assets/banking.png"),
                        name: "Banking Fraud",
                    },
                    {
                        img: require("../../assets/crypto.png"),
                        name: "Cryptocurrency",
                    },
                    {
                        img: require("../../assets/foxer.png"),
                        name: "Forex",
                    },
                    {
                        img: require("../../assets/dating.png"),
                        name: "Romance / Online Dating",
                    },
                    {
                        img: require("../../assets/binary.png"),
                        name: "Romance / Online Dating",
                    },
                    {
                        img: require("../../assets/cfd.png"),
                        name: "CFD Trading Scams",
                    },
                    {
                        img: require("../../assets/online-scams.png"),
                        name: "Online Scams",
                    },
                    {
                        img: require("../../assets/credit-card.png"),
                        name: "Credit/Debit Card Scams",
                    },
                ],

        }
    }
}
</script>

<style lang="scss" scoped>
@import "../../scss/Types.scss";
</style>