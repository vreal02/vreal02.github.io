<template>
    <figure>
        <article>
            
            <div class="circles">
                <div class="circle"></div>
                <div class="circle"></div>
                <div class="circle"></div>
            </div>

            <div class="bar"></div>

            <div class="circles" style="opacity: 0;">
                <div class="circle"></div>
                <div class="circle"></div>
                <div class="circle"></div>
            </div>

        </article>
        <img :src="src">
    </figure>
</template>

<script>
export default {
    props:{
		src: {
			type: String,
			required: true
		}
	}
}
</script>

<style lang="sass" scoped>
img
	// cursor: pointer
	width: 100%
	height: 100%
	transition: all .5s ease
	border-radius: 0 0 10px 10px 

figure article
	background: #EDEDED
	height: 20px
	border-radius: 10px 10px 0 0
	display: flex
	justify-content: space-between
	align-items: center


.circles
	width: 40px
	height: 100%
	display: flex
	justify-content: space-between
	align-items: center
	padding: 0 .5rem

.circle
	width: 5px
	height: 5px
	border-radius: 50%
	background: #C4CBD3

.bar
	width: 70px
	height: 12px
	border-radius: 2px
	background: #C4CBD3

</style>