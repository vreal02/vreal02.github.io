<template>

    <section class="main">
        
        <basic-title

            :title="{
                title: $t('projects.casino.title'),
                subtitle: $t('projects.casino.description')
            }"
            :isBold="true"
            :isGradient="true"
        />
        
        <article class="main-cards">

            <basic-card-image
                :text="$t('projects.casino.text1')"
                :image="'/casino/menu.png'"
            />
            <basic-card-image
                :text="$t('projects.casino.text2')"
                :image="'/casino/poker2.png'"
            />
            <basic-card-image
                :text="$t('projects.casino.text3')"
                :image="'/casino/horse1.png'"
            />
            <basic-card-image
                :text="$t('projects.casino.text4')"
                :image="'/casino/horse2.png'"
            />
            <basic-card-image
                :text="$t('projects.casino.text5')"
                :image="'/casino/bingo1.png'"
            />
            <basic-card-image
                :text="$t('projects.casino.text6')"
                :image="'/casino/bingo3.png'"
            />

        </article>

        <basic-button
            class="main-button"
            :text="$t('button.back')"
            :link="'/'"
        />

    </section>

  
</template>

<script>

    export default {
        layout: 'default',
        head: {
            title: 'Vicente Real Casino'
        }
    }
    
</script>

<style lang="sass" scoped>

.main
    padding: 1rem
    display: grid
    gap: 1rem
    @media (min-width: 780px)
        padding: 1rem 4rem

    &-cards
        display: grid
        gap: 1rem
        @media (min-width: 768px)
            grid-template-columns: 1fr 1fr
    
    &-button
        justify-self: flex-end

</style>