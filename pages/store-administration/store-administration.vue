<template>
	<view class="content">
		<view class="scroll-x" >
			<scroll-view class="navx" scroll-x="true" show-scrollbar="false">
				<view :class="['navx-item',index1===currentIndexX ? 'active' : '']" v-for="(item1,index1) in navx" :key="index1" @tap="taps(index1)">
					<view>{{item1}}</view>
				</view>
			</scroll-view>
		</view>
		<view class="">
			<view class="scroll-y" >
				<scroll-view class="navy" scroll-y="true" >
					<view :class="['navy-item',index2===currentIndexY ? 'activeY' : '']" v-for="(item2,index2) in navy" :key="index2" @tap='tapY(index2)'>
						<view>{{item2}}</view>
					</view>
				</scroll-view>
			</view>
			<view class="classify-name">
				大折扣 煲仔饭
			</view>
			<view class="store">
				<view class="store-item">
					<view class="img">
						<image src="../../static/img/images/0ec2a489ee414e19c6cde9efbaa15c5_03.png" mode=""></image>
					</view>
					<view class="info">
						<view class="foot-name">
							老面炸油条(民间小吃)66666666666666666666666666
						</view>
						<view class="Sale">
							月售3
						</view>
						<view class="money">
							<text>￥3</text>
							<text>￥5</text>
						</view>
						<view class="number">
							<view class="disappear">
								库存111
							</view>
							<view class="disappear">
								下架
							</view>
						</view>
					</view>
				</view>
				<view class="store-item">
					<view class="img">
						<image src="../../static/img/images/0ec2a489ee414e19c6cde9efbaa15c5_03.png" mode=""></image>
					</view>
					<view class="info">
						<view class="foot-name">
							老面炸油条(民间小吃)
						</view>
						<view class="Sale">
							月售3
						</view>
						<view class="money">
							<text>￥3</text>
							<text>￥5</text>
						</view>
						<view class="number">
							<view class="disappear">
								库存111
							</view>
							<view class="disappear">
								下架
							</view>
						</view>
					</view>
				</view>
			</view>
		</view>
		<view class="b-bottom">
			<view class="item">管理分类</view>
			<view class="item"><i class="iconfont icon-paixu" style="color: #eabe67;"></i>排序&批量</view>
			<view class="item"><i class="iconfont icon-zengjia-" style="color: #eabe67;"></i>新建商品</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				navx: [
					'全部',
					'热卖',
					'已下架',
					'售卖中',
					'已售空'
				],
				navy: [
					'大折扣 煲仔饭',
					'满减煲仔粥',
					'熬制炖汤',
					'大折扣,煲仔饭',
					'满减煲仔粥',
					'熬制炖汤',
					'大折扣,煲仔饭',
					'满减煲仔粥',
					'熬制炖汤',
					'满减煲仔粥',
					'熬制炖汤',
					'大折扣,煲仔饭',
					'满减煲仔粥',
					'熬制炖汤',
					'满减煲仔粥',
					'熬制炖汤',
					'大折扣,煲仔饭',
					'满减煲仔粥',
					'熬制炖汤'
				],
				ceshi: [
					{'name': 'zs', 'id': 0, 'gender': 'male'},
					{'name': 'ls', 'id': 1, 'gender': 'female'},
					{'name': 'ww', 'id': 2, 'gender': 'male'}
				],
				currentIndexX: 0,
				currentIndexY: 0,
			}
		},
		methods: {
			taps(e){
				console.log(e);
				this.currentIndexX=e
			},
			tapY(e){
				console.log(e);
				this.currentIndexY = e
			}
		}
	}
</script>

<style>
	.content {
		padding: 0;
	}
	.content {
		width: 100%;
		box-sizing: border-box;
		margin: 0 auto;
		background-color: #FFFFFF;
		}
		
	.navx {
	  white-space: nowrap;
	  padding: 5rpx 0;
	
	}
	.navx-item {
	  padding: 20rpx 45rpx;
	  font-size: 30rpx;
	  display: inline-block;
	  color: #9b9b9b;
	}
	.active {
		/* background-color: pink; */
		color: #3b3a3f;
	}
	.scroll-y {
		width: 180rpx;
		float: left;
	}
	.activeY {
		background-color: #FFFFFF;
		/* color: pink; */
		color: #3b3a3f;
		/* font-size: 100rpx; */
	}
	.navy {
	  padding: 5rpx 0;
	  height: 1050rpx;
	  width: 100%;
	  background-color: #f4f4f4;
	  color: #9b9b9b;
	
	}
	.navy-item {
	  padding: 20rpx 20rpx;
	  font-size: 30rpx;
	  
	}
	.store {
		display: inline;
		float: left;
		width: 70%;
		margin-left: 2%;
	}
	.store .store-item{
		/* background-color: pink; */
		/* padding-top: 20rpx; */
		/* height: 300rpx; */
		margin-top: 50rpx;
		/* border-bottom: 2rpx solid #8E8E8E; */
		padding-bottom: 20rpx;
	}
	.store .store-item .img {
		display: inline-block;
		float: left;
	}
	.store .store-item .img image {
		width: 140rpx;
		height: 140rpx;
		display: block;
	}
	.store .store-item .info {
		display: inline-block;
		margin-left: 16rpx;
		width: 360rpx;
	}
	.store .store-item .info .foot-name {
		font-size: 30rpx;
		font-weight: bold;
		overflow: hidden;
			text-overflow: ellipsis;
			white-space: nowrap;
		/* margin-top: 30rpx; */
	}
	.store .store-item .info .Sale {
		color: #8e8e8e;
		font-size: 25rpx;
	}
	.store .store-item .info .money {
		margin-bottom: 10rpx;
	}
	.store .store-item .info .money text:nth-child(1) {
		font-size: 35rpx;
		color: #ed5c59;
	}
	.store .store-item .info .money text:nth-child(2) {
		font-size: 20rpx;
		color: #d9d7d8;
		text-decoration:line-through;
		margin-left: 25rpx;
	}
	.store .store-item .info .number {
		
	}
	.store .store-item .info .number .disappear {
		border: 2rpx solid #cdcdcd;
		padding: 8rpx 4px;
		display: inline-block;
		width: 140rpx;
		text-align: center;
		font-size: 24rpx;
		color: #cdcdcd;
	} 
	.store .store-item .info .number .disappear:nth-child(2) {
		margin-left: 20rpx;
	}
	.classify-name {
		float: left;
		margin-left: 15rpx;
		padding-top: 30rpx;
		width: 70%;
		font-weight: bold;
	}
	.b-bottom {
		width: 100%;
		position: fixed;
		bottom: 0;
		display: flex;
		justify-content:space-around;
		padding: 30rpx 0;
		border-top: 2rpx solid #cdcdcd;
	}
	.b-bottom {
		width: 100%;
		position: fixed;
		bottom: 0;
		display: flex;
		justify-content:space-around;
	}
	.b-bottom .item {
		font-size: 30rpx;
	}
	.b-bottom .iconfont{
		font-size: 35rpx;
		margin-right: 10rpx;
	}
</style>
