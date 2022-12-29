<template>
    <article class="card">
        <decoration-image
            :src="image"
        />

        <p class="card-text">{{text}}</p>

    </article>
</template>

<script>
export default {

    props:{

        text:{
            type: String,
            required: true
        },

        image:{
            type: String,
            required: true
        }
    }

}
</script>

<style lang="sass" scoped>

.card
    padding: 1.5rem 1rem
    border: 1px solid #C4CBD3
    box-shadow: 0px 2px 8px rgba(196, 203, 211, 0.25)
    border-radius: 20px

    &-text
        padding-top: 1rem

</style>