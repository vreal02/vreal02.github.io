<template>
    <article class="scroll-container">
        <article class="scroll-mouse">

        </article>
        <article class="scroll-text">
            <p>SCROLL</p>
        </article>

    </article>
</template>

<script>
export default {

    mounted(){
        window.addEventListener('scroll', this.handleScroll)
    },
    
    methods: {
        handleScroll(){
            let y = window.scrollY
            let scroll = document.querySelector('.scroll-container').style

            y > 0 ? scroll.opacity = '0' : scroll.opacity = '1'
        }

    }

}
</script>

<style lang="sass" scoped>

@keyframes mouse
    0%
        transform: translateY(0px)
    100%
        transform: translateY(10px)

.scroll

    &-container
        padding: 1rem
        display: flex
        flex-direction: column
        align-items: center
        gap: 1rem
        transition: 3s

    &-mouse
        width: 40px
        height: 70px
        border: solid black 2px
        border-radius: 40px
        position: relative
        align-self: center
        animation-name: mouse
        animation-duration: 3s
        animation-iteration-count: infinite
        animation-direction: alternate
        
        &::after
            content: ''
            width: 6px
            height: 6px
            border-radius: 50%
            background: black
            position: absolute
            top: 10px
            left: 15px

    &-text
        align-self: center
        p
            letter-spacing: 2px
    
</style>

