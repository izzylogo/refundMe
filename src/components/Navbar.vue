<template>
  <nav>
    <div class="nav-cover">
        <div class="left">refundeee</div>
        <div class="middle">
            <ul>
                <li>
                    <router-link to="/">Home</router-link>
                </li>
                <li>
                    <router-link to="/about">About</router-link>
                </li>
                <li>
                    <router-link to="/how-works">How it works</router-link>
                </li>
                <li>
                    <router-link to="/complain">File Complain</router-link>
                </li>
            </ul>
        </div>
        <div class="right">Get Your Money Back</div>
        <div class="burger"
            @click="toggleNav"
        >
            <div class="line1"></div>
            <div class="line2"></div>
            <div class="line3"></div>
        </div>
    </div>
    <div v-if="toggle" class="media">
        <div class="media-cover">
            <ul>
                <li>Home</li>
                <li>About</li>
                <li>How it works</li>
                <li>Contact Us</li>
            </ul>
        </div>
    </div>
  </nav>
</template>

<script>
export default {
    name: 'Navbar',
    data() {
        return {
            toggle: false,
        }
    },
    methods: {
        toggleNav() {
            this.toggle = !this.toggle
        },
    },

}
</script>

<style lang="scss" scoped>
@import "../scss/Navbar.scss";

</style>