<template>

    <section class="main">
        
        <basic-title

            :title="{
                title: $t('projects.onroom.title'),
                subtitle: $t('projects.onroom.description')
            }"
            :isBold="true"
            :isGradient="true"
        />
        
        <article class="main-cards">

            <basic-card-image
                :text="$t('projects.onroom.text1')"
                :image="'/onroom/onroom_login.png'"
            />
            <basic-card-image
                :text="$t('projects.onroom.text2')"
                :image="'/onroom/onroom_home.png'"
            />
            <basic-card-image
                :text="$t('projects.onroom.text3')"
                :image="'/onroom/onroom_home_empty.png'"
            />
            <basic-card-image
                :text="$t('projects.onroom.text4')"
                :image="'/onroom/onroom_task.png'"
            />
            <basic-card-image
                :text="$t('projects.onroom.text5')"
                :image="'/onroom/onroom_task_empty.png'"
            />
            <basic-card-image
                :text="$t('projects.onroom.text6')"
                :image="'/onroom/onroom_popup.png'"
            />
            <basic-card-image
                :text="$t('projects.onroom.text7')"
                :image="'/onroom/onroom_doc.png'"
            />
            <basic-card-image
                :text="$t('projects.onroom.text8')"
                :image="'/onroom/onroom_calendar.png'"
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
            title: 'Vicente Real OnRoom'
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