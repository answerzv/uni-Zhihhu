<template>
	<view style="overflow:hidden" class="container">
		<swiper class="swiper"  :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
			<swiper-item  v-for="item in background">	
				<image  style="width: 100vw; "  :src="item"></image>
			</swiper-item>	   
		</swiper>
   </view>
	
</template>

<script>
	import data3 from '../static/data/index.js'
	export default{
		data(){
			return{
				myJson:data3,
				
				background: ['color1', 'color2', 'color3'],
									           
			    background: [ 
							 require('../images/24213.jpg'),
							 require('../images/24280.jpg'),
							 require('../images/1444983318907-_DSC1826.jpg')
						   ],
					
				indicatorDots: true,
				autoplay: true,
				interval: 2000,
				duration: 500
				
			}
		},
		onShow: function() {
			
		},
		methods:{
			
			
			changeIndicatorDots(e) {
			     this.indicatorDots = !this.indicatorDots
			},
			 
			 changeAutoplay(e) {
			     this.autoplay = !this.autoplay
			},
			 
			 intervalChange(e) {
			     this.interval = e.target.value
			 },
			  
			 durationChange(e) {
			     this.duration = e.target.value
			 }
		}
		
	}
</script>



<style>	
swiper{
	height: 200px;
}
</style>
