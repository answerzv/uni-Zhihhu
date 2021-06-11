<template>
	<view class="container" >
		<view class="feed-item"  v-for="item in myJson.data1 " @click="getLick(item)">
			<view class="feed-source">
			    <view   class="avatar">
				    <image  :src='item.feed_source_img'  class="item-more" role='img'></image>
			    </view> 
				<a >
					<text>{{item.feed_source_name}}{{item.feed_source_txt}}</text>
				</a>
				<image class="item-more"></image>
			</view>
			
			
			<view class="feed-content">
				<view class="question">
				    <a class="question-link"> 
					    <text>{{item.question}}</text>
				    </a>
				</view>
				<view class="answer-body">
				    <view>
					    <text class="answer-txt">{{item.answer_ctnt}}</text>
				    </view>
					<view class="answer-actions">
						<view class="like dot">
							<a>{{item.good_num}} 赞同</a>
						</view>
						<view class="comments dot">
							<a>{{item.comment_num}} 评论 </a>
						</view>
						<view class="follow-it">
							 <a>关注问题</a>
						</view>
					</view>
				</view>	  	
			</view>  
			
			
		</view>
	</view>
</template>

<script>
	import data3 from '../static/data/index.js'
	
	export default{
		data(){
			return{
				myJson:data3,
				Eeeid:25,
				Eeeids:23,
				
				
				
				//img:'../../images/icon9.jpeg'
			}
		},
		onShow: function() {
			console.log(this.myJson)
			console.log(this.img)
			
		},
		methods:{
			e(){
				console.log('4')
				console.log(this.myJson.data1)
				
				
			},
			
			getLick(i){
				console.log(i.feed_source_id)
				this.userId = i.feed_source_id
				
				
				
				if(i.feed_source_id == this.Eeeid || i.feed_source_id == this.Eeeids){
					
					uni.navigateTo({
						url:'/pages/details/details',			
					})
					console.log('调整')
				}else{
					uni.navigateTo({
						url:'/pages/detailsList/detailsList',			
					})
				}
				
			}
		}
		
	}
	
</script>

<style>
	
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
