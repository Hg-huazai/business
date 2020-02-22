<template>
	<view class="content">
		<view class="order-top">
			<view class="order-options">
				<view :class="['order-options-item',Inv==0?'inv-h-se':'']" @click="Inv=0">等待处理</view>
				<view :class="['order-options-item',Inv==1?'inv-h-se':'']" @click="Inv=1">历史订单</view>
			</view>
			<view class="search">搜索订单</view>
		</view>
		<view v-show="Inv == 0">
			<view class="nav1">
				<scroll-view class="nav" scroll-x="true" show-scrollbar="flase">
					<view class="nav_item" :class="[index=== currentIndex ? 'active' : '']" v-for="(item,index) in nav" :key="index" @tap="taps(index)">
						<view>{{item}}</view>
					</view>
				</scroll-view>
			</view>
			<view class="order">
				<view class="tips-top">
					<view class="tips">订小贴士单使用</view class="tips">
					<view class="new">NEW</view>
					<navigator url="#">查看 &gt;</navigator>
					<view class="clear"></view>
				</view>
				<view class="Study">快速学习入户高效使用订单模板</view class="tips">
			</view>
		</view>
		
		
		<view v-show="Inv == 1">
			<view class="nav1">
				<scroll-view class="nav" scroll-x="true" show-scrollbar="flase">
					<view class="nav_item" :class="[index=== currentIndex ? 'active' : '']" v-for="(item,index) in nav" :key="index" @tap="taps(index)">
						<view>{{item}}</view>
					</view>
				</scroll-view>
			</view>
			<view class="order">
				<view class="tips-top">
					<view class="tips">订贴士单使用</view class="tips">
					<view class="new">NEW</view>
					<navigator url="#">查看 &gt;</navigator>
					<view class="clear"></view>
				</view>
				<view class="Study">快速学习入户高效使用订单模板</view class="tips">
			</view>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				currentIndex:0,
				Inv:0,
				nav:[
					"推荐",
					"进行中",
					"新订单",
					"退款",
					"待出餐",
					"待发货",
					"待签收"
					]
				
			}
		},
		methods: {
			 taps(e) {
					console.log(e)
					this.currentIndex = e;
				}
		}
	}
</script>

<style>
	.order-options{
		background-color: #dedede;
		height: 100upx;
		display: flex; 
		border-bottom: 1px solid #C8C7CC;
		width: 350rpx;
		height: 90rpx;
		padding: 6px;
		box-sizing: border-box;
		/* display: inline-block; */
		float: left;
	}
	.order-top .search {
		/* display: inline-block; */
		background-color: #fff;
		display: flex; 
		/* height: 80rpx; */
		/* line-height: 80rpx; */
		float: right;
		padding: 10rpx 30rpx;
		border-radius: 40rpx;
		box-sizing: border-box;
		margin-top: 15rpx;
	}
	.order-options-item{
		font-size: 30upx;
		flex: 1;
		text-align: center;
		color: #C9C9C9;
		height: 71rpx; 
		line-height: 71rpx;
		color: #000000;
		border-radius: 20rpx;
		/* display: inline-block; */
		
		
	}
	.inv-h-se{
		color: #5BA7FF;
		/* border-bottom: 4upx solid #5BA7FF; */
		background-color: #FFFFFF;
	}
	.active {
		color: #900;
		border-bottom: 2px solid #900;
		margin: 0 auto;
		
	}
	.content {
		width: 100%;
		box-sizing: border-box;
		margin: 0 auto;
		}
		
	.nav {
	  white-space: nowrap;
	  padding: 5rpx 0;
	}
	.nav_item {
	  padding: 20rpx 45rpx;
	  font-size: 30rpx;
	  display: inline-block;
	}
	.order {
		margin-top: 60rpx;
		background-color: #fff;
		height: 245rpx;
		width: 100%;
		padding: 60rpx 50rpx;
		box-sizing: border-box;
	}
	
	.order .tips-top .tips {
		display: inline-block;
		margin-bottom: 35rpx;
		color: #000;
		float: left;
	}
	.order .tips-top .new {
		float: left;
		background-color: #ea6264;
		color: #FFFFFF;
		padding: 0 10rpx;
		font-size: 13rpx;
		border-radius: 18rpx;
		display: inline-block;
		margin-left: 10rpx;
		margin-top: 4rpx;
		
		
	}
	.order .tips-top navigator {
		display: inline-block;
		float: right;
		color: #989898;
	}
	.order .tips-top .clear {
		clear: both;
	}
	.order .Study {
		color: #989898;
		font-size: 20rpx;
	}
		
</style>
