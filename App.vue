<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	
	
	/deep/uni-swiper  .uni-swiper-wrapper{
		overflow:visible;
		
	}
	
	/deep/uni-image{
		overflow:visible
	}
	
	
	/deep/uni-swiper-item{
		overflow:visible
	}
	
	/deep/uni-swiper[data-v-5dabfba7]{
	     height: 229px!important;
	}
	
	
	
	
	/* /deep/uni-image>div, uni-image>img{
		width: 100vw;
	} */
</style>
