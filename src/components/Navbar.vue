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
        <div class="right">
            <router-link to="/complain">
                Get Your Money Back
            </router-link>
        </div>
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
                <li @click="toggle = false">
                    <router-link to="/">
                        Home
                    </router-link>
                </li>
                <li @click="toggle = false">
                    <router-link to="/about">
                        About
                    </router-link>
                </li>
                <li @click="toggle = false">
                    <router-link to="/how-works">
                        How it works
                    </router-link>
                </li>
                <li @click="toggle = false">
                    <router-link to="/complain">
                        Contact Us
                    </router-link>
                </li>
            </ul>
            <div class="button">
                <button @click="toggle = false">
                    <router-link to="/complain">Get Your Money</router-link>
                </button>

            </div>
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