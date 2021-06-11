<template>
	<view>
		<view class="chat-item flex-wrp" v-for="item in rc" >
			<view class="avatar flex-item">
				<image :src="item.img"></image>
			</view>
			<view class="chat-content flex-item">
				<view class="chat-source">
					<text class="chatmate">{{item.name}}</text>
					<text class="lasttime">{{item.s}}个月前</text>
				</view>
				<text class="chat-txt">你好~ 你好~ 你好~</text>
			</view>
		</view>
	</view>
		
		
		
		
</template>

<script>
	export default{
		data(){
			return{
				rc:[
					{img:require('../../images/icon8.jpg'),s:1,name:'Alex'},
					{img:require('../../images/icon9.jpeg'),s:3,name:"George"},
					]
			}
		}
	}
</script>

<style>
	.container {
	    height: 100%;
	    display: flex;
	    flex-direction: column;
	    align-items: center;
	    justify-content: space-between;
	    box-sizing: border-box;
	    background: #F0F4F3;
	}
	.container {
	    padding: 0;
	    font-size: 14rpx;
	    color: #000;
	}
	
	.flex-wrp {
	    display: flex;
	}
	.chat-item {
	    width: 725rpx;
	    background: #ffffff;
	    padding: 25rpx 25rpx 25rpx 0;
	    border-bottom: solid 1px #ebebeb;
	}
	
	.flex-item {
	    flex-grow: 1;
	    text-align: center;
	}
	.chat-item .avatar {
	    flex: 1;
	}
	
	.chat-item image {
	    width: 80rpx;
	    height: 80rpx;
	    border-radius: 80rpx;
	}
	
	.flex-item {
	    flex-grow: 1;
	    text-align: center;
	}
	.chat-item .chat-content {
	    flex: 4;
	    text-align: left;
	}
	
	.chat-item .chat-content .chat-source {
	    color: #818A8F;
	    font-size: 28rpx;
	    padding: 4rpx 0 8rpx 0;
	}
	
	.chat-item .chat-content .chat-source .chatmate {
	    font-size: 34rpx;
	    color: #000000;
	    text-align: left;
	}
	
	.chat-item .chat-content .chat-source .lasttime {
	    flex: 1;
	    font-size: 22rpx;
	    float: right;
	    vertical-align: text-bottom;
	}
	
	.chat-item .chat-content .chat-txt {
	    display: block;
	    color: #7b7b7b;
	    font-size: 26rpx;
	    line-height: 34rpx;
	}
	
	
</style>
