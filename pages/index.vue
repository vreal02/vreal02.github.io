<template>
    <section class="main">

        <section class="main-intro">
            <basic-header />
            <basic-title

                :title="{
                    title: 'Junior Web Developer'
                }"

                :isThin="true"
            
            />
            <scroll-down/>
        </section>

        <section class="main-skills">
            <article class="main-skills-container">
                <basic-title

                    :title="{
                        title: `Hi, I'm Vicente. Nice to meet you.`,
                        paragraph: `I'm a young programmer in training, organized and outgoing, I work both individually and in teams, I'm always willing to update myself and learn about new technologies. `
                    }"

                    :isBold="true"
                    :titleCenter="true"

                    class="jio"
            
                />

            </article>

            <article class="main-skills-cards">
                <article class="main-skills-cards-front">
                    <basic-title

                        :title="{
                            title: 'Front-end',
                            subtitle: 'I like to transform my own ideas, and see the result in the design.'
                        }"
                        
                        :isBold="true"
                        :isGradient="true"

                    />

                    <basic-list
                        :title="'Languajes I speak'"
                        :list="[
                            'HTML 5',
                            'CSS 3',
                            'Sass',
                            'JavaScript',
                            'Vue JS',
                            'Nuxt JS'
                        ]"
                    />

                </article>
                <article class="main-skills-cards-back">
                    <basic-title
                        
                        :title="{
                            title: 'Back-end',
                            subtitle: 'The unseen part of a website is also beautiful.'
                        }"
                        
                        :isBold="true"
                        :isGradient="true"
                        :titleCenter="true"

                    />

                    <basic-list
                        :title="'Languajes I speak'"
                        :list="[
                            'Python',
                            'Django',
                            'Java',
                            'Node JS',
                            'MySQL',
                            'MongoDB'
                        ]"
                    />

                </article>


            </article>
        </section>
        <section class="main-projects">
            <basic-title

                :title="{
                    title: 'My projects',
                    subtitle: 'Here you can see all my projects'
                }"
                :isBold="true"
                :titleCenter="true"
            
            />

            <basic-card
                :text="{
                    title: 'OnRoom',
                    paragraph: 'OnRoom is an educational software that, once implemented in a school, facilitates communication between students and teachers in a simple and intuitive way.'
                }"
                :button="{
                    text: 'See more',
                    link: '/onroom'
                }"

                :carousel="[
                    '/onroom/onroom_login.png',
                    '/onroom/onroom_home.png',
                    '/onroom/onroom_home_empty.png',
                    '/onroom/onroom_task.png',
                    '/onroom/onroom_task_empty.png',
                    '/onroom/onroom_popup.png',
                    '/onroom/onroom_doc.png',
                    '/onroom/onroom_doc_empty.png',
                    '/onroom/onroom_calendar.png',
                ]"
            />

            <basic-card
                :text="{
                    title: 'Casino Pythoniani',
                    paragraph: 'The pythoniani casino was my first group work as a programmer, in which I participated in three of the six games it has: poker, bingo and horse race, the difficulty of this project is that it is all console and very visual being python a backend language.'
                }"
                :button="{
                    text: 'See more',
                    link: '/casino'
                }"

                :carousel="[
                    '/casino/poker1.png',
                    '/casino/bingo1.png',
                    '/casino/horse1.png',
                    '/casino/poker2.png',
                    '/casino/bingo2.png',
                    '/casino/horse2.png',
                    '/casino/poker3.png',
                    '/casino/bingo3.png',
                    '/casino/horse3.png'
                ]"
            />

        </section>
        
    </section>

</template>


<script>

    export default{
        layout: 'default'
    }

</script>

<style lang="sass" scoped>

.main
    overflow: hidden

    &-intro
        height: 100vh
        display: flex
        flex-direction: column
        align-items: center
        justify-content: space-between

    &-skills
        height: 1000px
        position: relative
        @media (min-width: 800px)
            height: 800px

        &-container
            height: 50vh
            background: #667EEA
            color: white
            padding: 1rem 1rem
            @media (min-width: 480px)
                padding: 1rem 4rem

        &-cards
            width: calc(100% - 2rem)
            border: solid black
            position: absolute
            background: white
            top: 25%
            left: 1rem
            border: 1px solid #C4CBD3
            box-shadow: 0px 2px 8px rgba(196, 203, 211, 0.25)
            border-radius: 20px
            display: flex
            flex-direction: column

            @media (min-width: 480px)
                left: 4rem
                width: calc(100% - 8rem)
                display: flex

            @media (min-width: 780px)
                flex-direction: row

            &-front
                padding: 1rem
                display: flex
                flex-direction: column
                justify-content: flex-start
                align-items: flex-start
                gap: 1rem
                width: 100%
                border-bottom: 1px solid #C4CBD3

                @media (min-width: 780px)
                    border-bottom: none 
                    padding: 1rem 4rem
                    border-right: 1px solid #C4CBD3
                    width: 50%
            
            &-back
                padding: 1rem
                display: flex
                flex-direction: column
                justify-content: flex-start
                align-items: flex-start
                gap: 1rem
                width: 100%

                @media (min-width: 780px)
                    width: 50%
                    padding: 1rem 4rem

    &-projects
        display: flex
        flex-direction: column
        justify-content: center
        gap: 1rem
        align-items: center
        padding: 1rem 
        @media (min-width: 480px)
            padding: 5rem 4rem 1rem 4rem

        @media (min-width: 780px)
            padding: 1rem 4rem
            

</style>
