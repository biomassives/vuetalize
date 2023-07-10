<script setup lang="ts">
import FeatureCard from './FeatureCard.vue'

const features = [
    {
        title: 'Checkins',
        icon: 'i-iconoir-flash',
        description:
            ' Track activities that generate biodiversity credits & NFT tokens.',
    },
    {
        title: 'Verification',
        icon: 'i-iconoir-vue-js',
        description:
            'Community verifiers are trained to be experts in techniques most appropriate for their regionalcontext.',
    },
    {
        title: 'Techniques',
        icon: 'i-iconoir-path-arrow',
        description:
            'Biodiversity credit-worthy activities empower those effected by pollution & climate to restore damaged environment',
    },
    {
        title: 'Transparency',
        icon: 'i-iconoir-import',
        description: 'Participants provide checkin photos & recordings to show details about steps taken toward achieving project milestones',
    },
    {
        title: 'Verification Training',
        icon: 'i-iconoir-puzzle',
        description: 'Vue Use is a collection of useful composition functions for Vue.js.',
    },
    {
        title: 'Circular Ecomomy Partners',
        icon: 'i-iconoir-code',
        description:
            'Vue Use Head is a composition function for Vue.js that allows you to easily manage the document head.',
    },

    {
        title: 'Selling Biodiversity Credits',
        icon: 'i-iconoir-translate',
        description:
            'Vue i18n is internationalization plugin for Vue.js. It provides services for translating Vue component templates, directives, and parts of HTML.',
    },
    {
        title: 'Pinia',
        icon: 'i-iconoir-share-android',
        description: 'Pinia is a store for Vue.js applications. It is inspired by Vuex and uses a similar API.',
    },

    {
        title: 'Dark Mode',

        icon: 'i-iconoir-half-moon',
        description: 'The theme of the app is automatically set to dark mode based on your system settings.',
    },
]
</script>
<template>
    <section class="mt-4 d-flex flex-column align-center">
        <h2>
            {{ $t('hero.features.title') }}
        </h2>
        <v-row class="d-flex justify-start w-100 mt-16 flex-wrap">
            <v-col v-for="(feature, index) in features" :key="index">
                <FeatureCard :feature="feature" />
            </v-col>
        </v-row>
    </section>
</template>

<style scoped></style>
