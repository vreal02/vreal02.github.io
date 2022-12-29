<template>

    <hgroup>
        <h1 
            :class="[
                isThin ? 'isThin' : '',
                isBold ? 'isBold' : '',
                isGradient ? 'isGradient' : '',
                titleCenter ? 'titleCenter' : ''
            ]"
        >   
            {{title.title}}
        </h1>

        <p v-if="title.subtitle" class="isThin">{{title.subtitle}}</p>
        <p v-if="title.paragraph"> {{title.paragraph}} </p>
    </hgroup>
  
</template>

<script>
export default {

    props: {
        title: {
            type: Object,
            required: true
        },
        isThin: {
            type: Boolean,
            required: false,
            default: false
        },
        isBold: {
            type: Boolean,
            required: false,
            default: false
        },
        isGradient: {
            type: Boolean,
            required: false,
            default: false
        },
        titleCenter: {
            type: Boolean,
            required: false,
            default: false
        }
    }
}
</script>

<style lang="sass" scoped>

h1
    font-size: 24px
    @media (min-width: 480px)
        font-size: 36px

p
    @media (min-width: 723px)
        font-size: 22px

hgroup
    display: flex
    flex-direction: column
    gap: 1rem

.isBold
    font-family: 'Poppins Bold'

.isThin
    font-family: 'Poppins'

.isGradient
    background: linear-gradient(90deg, #667EEA , #764BA2 )
    width: fit-content
    -webkit-background-clip: text
    -webkit-text-fill-color: transparent

.titleCenter
    text-align: center

</style>