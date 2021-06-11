<template>
	<view>

	    <!-- 头部选项卡 -->

		<!-- <view class="head-nav">
	        <view :class="navIndex==1?'activite':''" @click="checkIndex(1)">推荐</view>
	        <view :class="navIndex==2?'activite':''" @click="checkIndex(2)">圆桌</view>
			<view :class="navIndex==3?'activite':''" @click="checkIndex(3)">热门</view>
	        <view :class="navIndex==4?'activite':''" @click="checkIndex(4)">收藏</view>
	    </view> -->

		   
		   
		<!-- 内容切换 -->
		   
		<!-- <view class="content" v-if="navIndex==1">
	       <Fa></Fa>
		   <In></In>
	    </view>
	    <view class="content" v-if="navIndex==2">
	      我是选项二
	    </view>
		<view class="content" v-if="navIndex==3">
		      我是选项3
		</view>
		<view class="content" v-if="navIndex==4">
		      我是选项4
		</view> -->





		<view class="head-nav">
			
			<!-- 头部选项卡 -->
			     <view :class="listIndex==y?'activite':''" @click="checkListIndex(y)" v-for="(item,y) in navList"
				:key="y">{{item}}</view>
		</view>


		<!-- 内容 -->
		<view class="content">

			 <view class="" v-if="listIndex==0">
			    <view class="box">
					<Fa></Fa>
				    <In></In>
				</view>
		     </view>

			<view class="" v-if="listIndex==1">
				<view class="box">圆桌11111</view>
		    </view>

			<view class="" v-if="listIndex==2">
				<view class="box">热门问题</view>
		    </view>

			<view class="" v-if="listIndex==3">
			    <view class="box">收藏问题</view>
		    </view>

			   
		</view>















	</view>
</template>

<script>
	import Fa from '../../components/Carousel.vue'
	import In from '../../components/index.vue'
	export default {
		data() {

			return {
				// navIndex:1,   
				navList: ["推荐", "圆桌", "热门", "收藏"],
				listIndex: 0


			}
		},
		components: {
			Fa,
			In
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

<style scoped>
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
		width: 25%;
		text-align: center;
		padding-bottom: 10rpx;
	}

	
</style>
