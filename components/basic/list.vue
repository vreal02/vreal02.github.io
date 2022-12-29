<template>
    <article>
        <p class="title">{{title}}</p>

        <ul class="list">
            <li v-for="(item, index) in list" :key="index"><p class="item">{{item}}</p></li> 
        </ul>
    </article>
</template>

<script>
export default {

    props: {
        title: {
            type: String,
            required: false

        },
        list: {
            type: Array,
            required: true
        }
    }

}
</script>

<style lang="sass" scoped>

.title
    color: #667EEA
    
.title, .item
    @media (min-width: 480px)
        font-size: 22px

.list
    list-style: none
    padding-left: 2rem


</style>