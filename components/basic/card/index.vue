<template>

    <article class="card">
        <article class="card-info">

            <basic-title
            
                :title="{
                    title: text.title,
                    paragraph: text.paragraph
                }"

                :isBold="true"
            />

            <basic-button
                :text="button.text"
                :link="button.link"
            
            />


        </article>
        <article class="card-media">

            <carousel
                :images="carousel"
            />

        </article>
    </article>
</template>

<script>
export default {

    props:{

        text:{
            type: Object,
            required: true
        },

        button:{
            type: Object,
            required: true
        },

        carousel: {
            type: Array,
            required: true
        }
    }

}
</script>

<style lang="sass" scoped>

.card
    padding: 1rem
    border: 1px solid #C4CBD3
    box-shadow: 0px 2px 8px rgba(196, 203, 211, 0.25)
    border-radius: 20px
    display: flex

    &-info
        display: flex
        flex-direction: column
        justify-content: center
        align-items: flex-end
        gap: 1rem
        @media (min-width: 1024px)
            width: 60%
            padding-right: 1rem
            // border: solid 1px red

    &-media
        display: none
        @media (min-width: 1024px)
            // border: solid 1px red
            display: flex
            justify-content: center
            align-items: center
            width: 40%
            overflow: hidden

</style>