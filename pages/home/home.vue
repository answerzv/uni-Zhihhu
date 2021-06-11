<template>
	<view class="container">
		<view class="search flex-wrp">
		      <view class="search-left flex-item">
		          <image src="../../images/search.png"></image>
		          <input placeholder="搜索话题, 问题或人" placeholder-class="search-placeholder"/>
		      </view>
		      <view class="search-right flex-item" bindtap="upper">
		          <image src="../../images/lighting.png"></image>
		      </view>
			  
		 </view>
		 <view>
		 	 <In></In>
			 <In></In>
			 <In></In>
			 <In></In>
		 </view>
		 
		  
		  
		  
		  
	</view>
</template>

<script>
	import data3 from '../../static/data/index.js'
	import In from '../../components/index.vue'
	export default{
		data(){
			return{
				myJson:data3,
				
				//img:'../../images/icon9.jpeg'
			}
		},
		components: {
		
			In
		},
		onShow: function() {
			console.log(this.myJson)
			console.log(this.img)
			// for(let i = 0 ;i<this.myJson.data1.length; i++){
			// 	console.log(this.myJson.data1[i].feed_source_img)
			// 	this.img2= this.myJson.data1[i].feed_source_img
			// }
		},
		methods:{
			e(){
				console.log('4')
				console.log(this.myJson.data1)
				
				
			}
		}
		
	}
	
</script>

<style>
	
	
	.container .search .search-left image {
	    display: inline-block;
	    width: 35rpx;
	    height: 35rpx;
	    padding: 15rpx 15rpx 15rpx 20rpx;
	}
	
	.container .search .search-right image {
	    width: 45rpx;
	    height: 45rpx;
	    padding: 10rpx;
	}
	
	.flex-item {
	    flex-grow: 1;
	    text-align: center;
	}
	.container .search-left {
	    flex: 27;
	    background: #4EA3E7;
	    text-align: left;
	}
	
	.flex-wrp {
	    display: flex;
	}
	.container .search {
	    width: 735rpx;
	    height: 65rpx;
	    padding: 12.5rpx 0 12.5rpx 15rpx;
	    background: #2A8CE5;
	}
	
	
	.container {
	    height: 100%;
	    display: flex;
	    flex-direction: column;
	    align-items: center;
	    justify-content: space-between;
	    box-sizing: border-box;
	    background: #F0F4F3;
	}
	
	.container .search-left input {
	    display: inline-block;
	    height: 65rpx;
	    font-size: 26rpx;
	}
	
	.container .feed-item {
	    width: 690rpx;
	    padding: 30rpx 30rpx 20rpx;
	    margin: 7rpx 0 6rpx 0;
	    background: #ffffff;
	    border-top: 1px solid #eee;
	    border-bottom: 1px solid #eee;
	    box-shadow: 0 2px 5px #eeeeee;
	}
	
	.container .feed-item .feed-source {
	    width: 690rpx;
	    left: 0;
	    height: 50rpx;
	}
	
	.container .feed-item .feed-source .item-more {
    display: inline-block;
    width: 40rpx;
    height: 45rpx;
    float: right;
}

.container .feed-item .feed-content {
    padding: 10rpx 0 0 0;
}

.container .feed-item .feed-content .answer-page {
    padding: 10rpx 0 0 0;
    font-size: 24rpx;
    line-height: 28rpx;
    color: #5b5b5b;
}

.container .feed-item .feed-content .answer-actions {
    width: 690rpx;
    padding: 10rpx 0 0;
    color: #a0acac;
}

.container .feed-item .feed-content .answer-actions view {
    display: inline-block;
    vertical-align: text-bottom;
    padding: 0 10rpx 0 0;
    font-size: 24rpx;
}

.container .feed-item .feed-source text {
    display: inline-block;
    height: 40rpx;
    line-height: 20rpx;
    vertical-align: middle;
    margin: 0 0 0 15rpx;
    color: #a0acac;
    font-size: 26rpx;
}

.container .feed-item .feed-source .avatar {
    position: relative;
    display: inline-block;
}

.container .feed-item .feed-source a {
    display: inline-block;
    height: 40rpx;
}

.container .feed-item .feed-content .answer-txt {
    padding: 10rpx 0 0 0;
    font-size: 14px;
    line-height: 28rpx;
    color: #5b5b5b;
}
	
	
</style>
