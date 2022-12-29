<template>

    <section class="main">
        
        <basic-title

            :title="{
                title: 'OnRoom',
                subtitle: 'OnRoom is an educational software that, once implemented in a school, facilitates communication between students and teachers in a simple and intuitive way.'
            }"
            :isBold="true"
            :isGradient="true"
        />
        
        <article class="main-cards">

            <basic-card-image
                :text="'This image represents the login screen, where the user registers, you can see that it is simple and friendly to avoid possible confusions, this section consists of two main parts: a decorative image and a very practical form. Finally above the form you can see the logo of the application made by me.'"
                :image="'/onroom/onroom_login.png'"
            />
            <basic-card-image
                :text="`Here you can see the home screen, which highlights different things, the student's pending tasks, notifications, and the weather (with the help of an external api specialized in providing weather data), on the left side you can see the menu with the different options that the user has to navigate through the application.`"
                :image="'/onroom/onroom_home.png'"
            />
            <basic-card-image
                :text="'This would be the home screen if the student had no notifications, had all the tasks done and had not activated the location in the browser.'"
                :image="'/onroom/onroom_home_empty.png'"
            />
            <basic-card-image
                :text="'This screen represents the homework page, where the user, depending on the subject he/she chooses, will be shown the homework of this subject, and also the status of the homework, if it has expired, if it has been handed in or if it can still be handed in.'"
                :image="'/onroom/onroom_task.png'"
            />
            <basic-card-image
                :text="'Here is what the homework page would look like if the user has not yet selected a subject.'"
                :image="'/onroom/onroom_task_empty.png'"
            />
            <basic-card-image
                :text="'In this image the popup to upload a task is represented, the whole background is dark to focus the user on the content of the center.'"
                :image="'/onroom/onroom_popup.png'"
            />
            <basic-card-image
                :text="'This screen represents the documents page, where the user, depending on the subject he/she chooses, will be shown the documents of this subject, and clicking on the visualize button will show the document.'"
                :image="'/onroom/onroom_doc.png'"
            />
            <basic-card-image
                :text="'The calendar page shows the tasks to be delivered but in a more visual way.'"
                :image="'/onroom/onroom_calendar.png'"
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