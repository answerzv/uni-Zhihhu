<template>
	<view>
		<view class="container more">
			<view class="user flex-wrp">
				<view class="avatar flex-item">
					<image role='img' class="userinfo-avatar" src="https://thirdwx.qlogo.cn/mmopen/vi_32/POgEwh4mIHO4nibH0KlMECNjjGxQUq24ZEaGT4poC6icRiccVGKSyXwibcPq4BWmiaIGuG1icwxaQX6grC9VemZoJ8rg/132" ></image>
				</view>
				<view class="user-info flex-item">
					<text class="userinfo-nickname">微信用户</text>
					<text class="edit">查看或编辑个人主页 </text>
				</view>
			</view>
			
			<view class="my">
				<view class="my-item flex-wrp" v-for="item in we">
					<view class="myitem-icon flex-item">
						<image :src='item.img'></image>
					</view>
					<view class="myitem-name flex-item">
						<text>{{item.text}}</text>
					</view>
					
				</view>
			</view>
			
		</view>
	</view>
</template>

<script>
	export default {
		data(){
			return{
				we:[
					{img:require('../../images/eye.png'),text:'我的关注'},
					{img:require('../../images/star.png'),text:'我的收藏'},
					{img:require('../../images/draft.png'),text:'我的草稿'},
					{img:require('../../images/recent.png'),text:'最近浏览'},
					{img:require('../../images/book.png'),text:'我的书架'},
					{img:require('../../images/live.png'),text:'我的Live'},
					{img:require('../../images/zhi.png'),text:'我的值乎'}
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
	.user {
	    width: 725rpx;
	    background: #ffffff;
	    padding: 30rpx 25rpx 30rpx 0;
	    margin: 15rpx 0 0 0;
	    border-top: 1px solid #eee;
	    border-bottom: 1px solid #dcdcdc;
	    box-shadow: 0 2px 5px #eeeeee;
	}
	
	.flex-item {
	    flex-grow: 1;
	    text-align: center;
	}
	
	.user .userinfo-avatar {
	    flex: 1;
	    display: inline-block;
	    width: 100rpx;
	    height: 100rpx;
	    border-radius: 80rpx;
	}
	
	.flex-item {
	    flex-grow: 1;
	    text-align: center;
	}
	.user .user-info {
	    flex: 5;
	    text-align: left;
	}
	
	.user .user-info text {
	    display: block;
	}
	.user .user-info .userinfo-nickname {
	    padding: 8rpx 0 10rpx 0;
	    font-size: 30rpx;
	    color: #818A8F;
	}
	
	.user .user-info text {
	    display: block;
	}
	.user .user-info .edit {
	    font-size: 30rpx;
	    color: #bababa;
	    line-height: 34rpx;
	}
	
	.my {
	    margin: 15rpx 0 0 0;
	    border-top: solid 1px #ebebeb;
	    border-bottom: solid 2px #ebebeb;
	}
	
	.flex-wrp {
	    display: flex;
	}
	.my .my-item {
	    width: 750rpx;
	    background: #ffffff;
	    padding: 0;
	}
	
	.flex-item {
	    flex-grow: 1;
	    text-align: center;
	}
	.my .my-item .myitem-icon {
	    flex: 1;
	}
	
	.my .my-item .myitem-icon image {
	    width: 45rpx;
	    height: 45rpx;
	    padding: 37.5rpx 0;
	}
	
	.flex-item {
	    flex-grow: 1;
	    text-align: center;
	}
	.my .my-item .myitem-name {
	    flex: 5;
	    text-align: left;
	    font-size: 34rpx;
	    color: #6d6d6d;
	    line-height: 60rpx;
	    padding: 30rpx 0;
	    border-bottom: solid 1px #ebebeb;
	}
	
	/deep/.user .userinfo-avatar div{
	    flex: 1;
	    display: inline-block;
	    width: 100rpx;
	    height: 100rpx;
	    border-radius: 80rpx!important;
	}
	
</style>
