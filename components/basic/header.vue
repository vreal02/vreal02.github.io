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

            <a href="https://www.linkedin.com/in/vicente-real-lafarga-942724242/" target="blank">
                <img src="/icons/linkedin.svg" width="30px">  
            </a>

            <a href="https://github.com/vreal02" target="blank">
                <img src="/icons/github.svg" width="30px" >  
            </a>

            <select v-model="selectedValue" @change="onChange(selectedValue)" >
                <option
                    v-for="(locale, index) in $i18n.locales"
                    :key="index"
                    :value="locale.code"
                >
                
                    {{locale.name}}

                    
                
                </option>
            </select>            

        </article>
    </header>
</template>

<script>
export default {
    data() {
        return {
            selectedValue: ""
        };
    },
    created() {
        this.selectedValue = this.$i18n.locale;
    },
    methods: {
        onChange(event) {
            this.$router.replace(this.switchLocalePath(event));
        }
  }

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

select
    border: none
    outline: none
    &:hover
        text-decoration: underline
        font-weight: bold
        cursor: pointer

option
    border-radius: none

</style>