<template>
    <section class="container">
		<article id="carousel">
		    
			<decoration-image v-for="(item,index) in images" :key="index"
				:src="item"
			
			/>

		</article>
	</section>
</template>

<script>
export default {

	props:{
		images: {
			type: Array,
			required: true
		}
	}

}
</script>

<style scoped>

.container{
	margin: 4% auto;
	width: 210px;
	height: 140px;
	position: relative;
	perspective: 800px;
}
#carousel{
	width: 100%;
	height: 100%;
	position: absolute;
	transform-style: preserve-3d;
	animation: rotation 25s infinite linear;
}
#carousel:hover{
	animation-play-state: paused;
}
#carousel figure{
	display: block;
	position: absolute;
	width: 186px;
	height: 116px;
	left: 10px;
	top: 10px;
	
	overflow: hidden;
	border-radius: 0 0 10px 10px;
}
p{
	position: absolute;
	top: 0;
}
#carousel figure:nth-child(1) { transform: rotateY(0deg) translateZ(288px);}
#carousel figure:nth-child(2) { transform: rotateY(40deg) translateZ(288px);}
#carousel figure:nth-child(3) { transform: rotateY(80deg) translateZ(288px);}
#carousel figure:nth-child(4) { transform: rotateY(120deg) translateZ(288px);}
#carousel figure:nth-child(5) { transform: rotateY(160deg) translateZ(288px);}
#carousel figure:nth-child(6) { transform: rotateY(200deg) translateZ(288px);}
#carousel figure:nth-child(7) { transform: rotateY(240deg) translateZ(288px);}
#carousel figure:nth-child(8) { transform: rotateY(280deg) translateZ(288px);}
#carousel figure:nth-child(9) { transform: rotateY(320deg) translateZ(288px);}



@keyframes rotation{
	from{
		transform: rotateY(0deg);
	}
	to{
		transform: rotateY(360deg);
	}
}

</style>