<template>
	<view>
		<view class="head-nav">
			
			<!-- 头部选项卡 -->
			     <view :class="listIndex==y?'activite':''" @click="checkListIndex(y)" v-for="(item,y) in navList"
				:key="y">{{item}}</view>
		</view>
		
		
		<!-- 内容 -->
		<view class="content">
		
			 <view class="" v-if="listIndex==0">
			    <view class="box">
					<view class="unrend">
						<text>0条未读</text>
						<image class="a" src="../../images/allread.png"></image>
					</view>
					<view class="notify-item flex-wrp" v-for=" item in data">
						<view class="avatar flex-item">
							<image src='../../images/icon1.jpeg'></image>
						</view>
						<view class="notify-content flex-item">
							<text class="notify-source">Rebecca回答了问题</text>
							<text class="notify-title">C#如何在不覆盖原有文件的情况下直接修改某一部分的内容？</text>
						</view>
					</view>
				</view>
		     </view>
		
			<view class="" v-if="listIndex==1">
				<view class="box">2</view>
		    </view>
		
			<view class="" v-if="listIndex==2">
				<view class="box">3</view>
		    </view>
		
			
		
			   
		</view>
	</view>
</template>

<script>
	
	export default {
		data() {
	
			return {
				 
				navList: ["通知", "赞与感谢", "关注"],
				listIndex: 0,
	
	            data:[1,2,3,4,5,6,7],
			}
		},
		
		methods: {
			checkIndex(index) {
				this.navIndex = index;
			},
	
			checkListIndex(index) {
				this.listIndex = index;
			}
	
	
	
		}
	}
</script>

<style>
	.head-nav {
		width: 100%;
		color: #8CCEFD;
		display: flex;
		justify-content: space-around;
		/* align-items: center; */
		background-color: #298DE5;
		height: 44px;
		line-height: 44px;
	}
	
	.activite {
		font-weight: bold;
		border-bottom: 3px solid #fff;
		color: #fff;
	}
	
	.head-nav>view {
		width: 33.3%;
		text-align: center;
		padding-bottom: 10rpx;
	}
	
	.unrend {
	    color: #9A9C9B;
	    height: 60rpx;
	    padding: 10rpx 40rpx;
	    text-align: left;
	    width: 670rpx;
		background-color:#F0F4F3 ;
	}
	
	.unrend text{
		display: inline-block;
		line-height: 60rpx;
		font-size: 22rpx;
	}
	
	.unrend image{
		display: inline-block;
		width: 50rpx;
		height: 50rpx;
		vertical-align: middle;
		float: right;
	}
	
	
	.flex-wrp {
	    display: flex;
	}
	.notify-item {
	    width: 680rpx;
	    background: #ffffff;
	    padding: 25rpx 70rpx 25rpx 0;
	    border-bottom: solid 1px #ebebeb;
	}
	
	.flex-item {
	    flex-grow: 1;
	    text-align: center;
	}
	.notify-item .avatar {
	    flex: 1;
	}
	
	.notify-item image {
	    width: 80rpx;
	    height: 80rpx;
	    border-radius: 80rpx;
	}
	
	.flex-item {
	    flex-grow: 1;
	    text-align: center;
	}
	.notify-item .notify-content {
	    flex: 4;
	    text-align: left;
	}
	
	.notify-item .notify-content text {
	    display: block;
	}
	.notify-item .notify-content .notify-source {
	    color: #818A8F;
	    font-size: 28rpx;
	    padding: 0 0 8rpx 0;
	}
	
	.notify-item .notify-content text {
	    display: block;
	}
	.notify-item .notify-content .notify-title {
	    color: #AFAFAF;
	    font-size: 30rpx;
	    line-height: 34rpx;
	}
	
</style>
