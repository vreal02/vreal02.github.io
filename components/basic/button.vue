<template>

    <nuxt-link class="button" :to="localePath(link)">{{ text }}</nuxt-link>
    
</template>

<script>
export default {
    props: {
        text: {
            type: String,
            required: true
        },
        link: {
            type: String,
            required: true
        }
    }

}
</script>

<style lang="sass" scoped>

.button
    text-decoration: none
    color: white
    background: #667EEA
    padding: .5rem 1rem
    border-radius: 6px

</style>