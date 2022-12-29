<template>

    <section class="main">
        
        <basic-title

            :title="{
                title: 'Casino Pythoniani',
                subtitle: 'The pythoniani casino was my first group work as a programmer, in which I participated in three of the six games it has: poker, bingo and horse race, the difficulty of this project is that it is all console and very visual being python a backend language.'
            }"
            :isBold="true"
            :isGradient="true"
        />
        
        <article class="main-cards">

            <basic-card-image
                :text="'The main menu of the casino was also designed by me, in this screen you can select the game mode you want to play.'"
                :image="'/casino/menu.png'"
            />
            <basic-card-image
                :text="'The poker game was by far the most expensive to program because there were many variables within the game, I had to recreate a small AI for the CPU, and designing the board was also complicated, it took me almost 3 months to program it but I managed to do it.'"
                :image="'/casino/poker2.png'"
            />
            <basic-card-image
                :text="'This is the first part of the horse race in which the user can bet on different horses to get more chips.'"
                :image="'/casino/horse1.png'"
            />
            <basic-card-image
                :text="'This is the second part of the horse race, it is totally automatic and the user only enjoys the race, at the end of the race the horse that has won is seen and the distribution of chips is done.'"
                :image="'/casino/horse2.png'"
            />
            <basic-card-image
                :text="'You can see the bingo ascii menu, in which you can select one, two or three cards, depending on the number you select you will have more or less probability of winning a prize.'"
                :image="'/casino/bingo1.png'"
            />
            <basic-card-image
                :text="'This is the second part of the bingo, it is played automatically after purchasing the cards from the previous menu, numbers are randomly drawn and are crossed out if the user has them on the card.'"
                :image="'/casino/bingo3.png'"
            />

        </article>

        <basic-button
            class="main-button"
            :text="'Back'"
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