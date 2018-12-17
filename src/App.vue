<template>
    <div id="app">
        <nav class="navbar">
            <div class="container">
                <div class="navbar-start">
                    <a class="navbar-item" href="#">MyCompany</a>
                </div>
                <span class="navbar-burger" v-on:click="toggleNav" v-bind:class="{'is-active': isActive}">
                  <span></span>
                  <span></span>
                  <span></span>
                </span>
                <div class="navbar-end navbar-menu" v-bind:class="{'is-active': isActive}" >
                    <router-link to="/" class="navbar-item r-item">Home</router-link>
                    <router-link to="/faq" class="navbar-item r-item">Features</router-link>
                    <router-link to="/faq" class="navbar-item r-item">About</router-link>
                    <router-link to="/faq" class="navbar-item r-item">Faq</router-link>
                    <div class="navbar-item">
                       <div class="buttons">
                           <a class="button is-primary is-outlined" href="">
                            <span class="icon">
                                <i class="fas fa-download"></i>
                            </span>
                               <span>Join Now</span>
                           </a>
                       </div>
                    </div>
                </div>
            </div>
        </nav>
        <router-view/>

        <footer class="footer is-primary">
            <div class="container">
                <div class="columns">
                    <div class="column">
                        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid aspernatur dolorem eius, esse inventore ipsa odio praesentium voluptas voluptates. Accusamus dolore doloribus eum explicabo odit quam, quos recusandae veniam voluptates.</p>
                    </div>
                    <div class="column has-text-right">
                        <a class="button is-primary">
                            <span class="icon">
                              <i class="fab fa-facebook"></i>
                            </span>
                            <span>Facebook</span>
                        </a>
                        <a class="button is-primary">
                            <span class="icon">
                              <i class="fab fa-twitter"></i>
                            </span>
                            <span>Twitter</span>
                        </a>
                    </div>
                </div>
            </div>
        </footer>
    </div>
</template>

<script>
    export default {
        name: 'App',
        data: function () {
            return {
                isActive: false
            }
        },
        methods: {
            toggleNav: function () {
                this.isActive = !this.isActive;
            }
        }
    }
</script>

<style lang="sass">
    @import '../node_modules/bulma/bulma.sass'
    @import "mq"

    .navbar
        background-color: #383838
        a:hover
            color: gray

        .navbar-start
            a
                color: #fff
                font-weight: bold
            a:hover
                color: gray

        a.r-item
            color: #c1c1c1
            padding: 0.5rem 1.75rem
            +mobile
                color: gray
                &:hover
                    background-color: #f1f1f1
    .navbar-burger span
        background-color: #c1c1c1

    footer
        background-color: $primary !important
        color: white
</style>
