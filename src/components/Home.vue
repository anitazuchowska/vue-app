<template>
    <div class="home">
        <section class="hero is-medium is-bold">
            <div class="hero-body">
                <div class="container">
                    <h1 class="title">
                       {{ heading }}
                    </h1>
                    <div class="is-two-thirds column is-paddingless">
                        <h2 class="subtitle is-4">{{ subheading }}</h2>
                    </div>
                    <a class="button is-large is-primary" id="learn" href="#">Learn more</a>
                </div>
            </div>
        </section>
        <section>
            <div class="container">
                <div class="columns pd is-desktop">
                    <div class="column is-1 has-text-centered">
                        <i class="fas fa-cog is-primary"></i>
                    </div>
                    <div class="column is-one-third-desktop">
                        <p class="title"><strong>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolore dolorum eaque error eveniet fuga incidunt </strong></p>
                    </div>
                    <div class="column is-one-third-desktop">
                        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolore dolorum eaque error eveniet fuga incidunt ipsam mollitia</p>
                    </div>
                </div>
                <div class="columns pd">
                    <div class="column">
                        <div class="card">
                            <div class="card-content">
                                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Amet consequuntur delectus deserunt est excepturi </p>
                                <p class="subtitle">- Anita Żuchowska</p>
                            </div>
                        </div>
                    </div>
                    <div class="column">
                        <div class="card">
                            <div class="card-content">
                                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Amet consequuntur delectus deserunt est excepturi </p>
                                <p class="subtitle">- Anita Żuchowska</p>
                            </div>
                        </div>
                    </div>
                    <div class="column">
                        <div class="card">
                            <div class="card-content">
                                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Amet consequuntur delectus deserunt est excepturi</p>
                                <p class="subtitle">- Anita Żuchowska</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
    export default {
        name: 'home',
        data() {
            return {
                heading : "Soaring to new heights",
                subheading: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid aspernatur dolorem eius, esse inventore ipsa odio praesentium voluptas voluptates. Accusamus dolore doloribus eum explicabo odit quam, quos recusandae veniam voluptates."
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
    @import "../mq"

    .hero
        background: url('../assets/clouds.jpg')
        background-size: cover
        background-position: bottom
    .title
        +mobile
            font-weight: bold
        +tablet
            font-size: 2rem
        +desktop
            font-size: 2rem
            margin-top: 2rem
    p
        +mobile
            font-weight: bold
        +tablet
            font-size: 1.5rem
        +desktop
            font-size: 1.5rem
            margin-top: 2rem
    h2
        margin: 1.5rem 0 2rem
    .fa-cog
        +desktop
            font-size: 2rem
            margin-top: 2.5rem
    #learn
        +desktop
            margin-bottom: 20px
    .pd
        +tablet
            padding: 2em 0
</style>
