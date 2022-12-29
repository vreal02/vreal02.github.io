<template>
    <header>
        <basic-title

            :title="{
                title: 'Vicente Real',
            }"

            :isBold="true"
            :isGradient="true"
        
        />
        <article class="icons">
            <a href="https://github.com/vreal02" target="blank">
                <img src="/icons/github.svg" width="30px" >  
            </a>
            
            <a href="https://www.linkedin.com/in/vicente-real-lafarga-942724242/" target="blank">
                <img src="/icons/linkedin.svg" width="30px">  
            </a>

        </article>
    </header>
</template>

<script>
export default {

}
</script>

<style lang="sass" scoped>

header
    padding: .5rem
    width: 100%
    display: flex
    justify-content: space-between
    // border: solid 1px green

.icons
    width: 100px
    display: flex
    justify-content: space-around
    align-items: center
    a
        display: flex
        align-items: center

    @media (min-width: 480px)
        width: 160px
        a        
            img
                width: 40px

</style>