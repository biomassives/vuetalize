<script setup lang="ts"></script>

<template>
    <section class="d-flex">
        <div class="glow glow-left"></div>
        <div class="glow glow-right"></div>
        <v-row style="flex: unset" class="hero-wrapper">
            <v-col sm="12" md="6">
                <div class="d-flex flex-column justify-center align-center h-100 hero min-h-screen">
                    <div class="d-flex flex-column">
                        <h1 class="tagline">
                            {{ $t('hero.title') }}
                        </h1>
                        <p class="text-muted py-8 description">{{ $t('hero.subtitle') }}</p>
                    </div>

                    <div class="d-flex justify-start w-100 space-x-2 rtl:space-x-reverse">
                        <v-btn color="primary-darken-1" to="/dashboard/overview" class="">
                            {{ $t('hero.dashboard') }}
                        </v-btn>
                        <v-btn
                            color="secondary"
                            variant="outlined"
                            href="https://github.com/boussadjra/vuetalize"
                            class="ml-8"
                            prepend-icon="mdi-github"
                            target="_blank"
                        >
                            {{ $t('hero.github') }}
                        </v-btn>
                    </div>
                </div>
            </v-col>
            <v-col sm="12" md="6" class="d-flex align-center justify-center logo">
                <Logo />
            </v-col>
        </v-row>
    </section>
</template>
<style scoped>
.hero-wrapper {
    z-index: 5;
}
.hero-wrapper .hero {
    max-width: 640px;
}
.tagline {
    font-weight: 800;
    line-height: 1.2;
    font-size: 2.8rem;
    background: linear-gradient(-312deg, #06926f 2%, #d69509 100%);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

html[dir='rtl'] .tagline {
    line-height: 1.6;
}
.v-theme--light .tagline {
    color: #1a8511;
    background: inherit;
    background-clip: unset;
    -webkit-background-clip: unset;
    -webkit-text-fill-color: inherit;
}

.v-theme--light .vuetify3 {
    background: linear-gradient(-312deg, #559620 2%, #bb9c13 100%);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}
.description {
    max-width: 620px;
    font-weight: 300;
    line-height: 1.5;
}

.min-h-screen {
    min-height: 100vh;
}

.logo {
    z-index: 5;
}
.glow {
    position: absolute;
    top: 0;
    left: 0;
    width: 400px;
    height: 800px;
    z-index: 0;
    background-image: linear-gradient(135deg, #07e250 -50%, #181833 30%);
}

.v-theme--light .glow {
    background-image: linear-gradient(135deg, #13d30d -50%, #efefef 30%);
}

.glow-right {
    right: 0;
    left: unset;
    z-index: 0;
    background-image: linear-gradient(-135deg, #1c960c -50%, #181833 30%);
}

.v-theme--light .glow-right {
    background-image: linear-gradient(-135deg, #298612 -50%, #efefef 30%);
}
</style>
