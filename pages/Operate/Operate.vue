<template>
	<view class="content">
		
		<view class="top">
			<view class="top-item">
				<view class="number">
					0
				</view>
				
				<view class="number2">
					今日订单收入/元
				</view>
			</view>
			<view class="top-item">
				<view class="number">
					0
				</view>
				<view class="number2">
					今日单量/单
				</view>
			</view>
		</view>
		<view class="spread">
			<!-- <view class="spread-top">
				<navigator url="">
					<view class="img">
						<image src="../../static/img/images/images/mendian1.png" mode=""></image>
					</view>
					<view class="text">
						<view class="text1">
							门店推广
						</view>
						<view class="text2">
							提升排名，流量法宝
						</view>
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<image src="../../static/img/images/images/mendian1.png" mode=""></image>
					</view>
					<view class="text">
						<view class="text1">
							门店推广
						</view>
						<view class="text2">
							提升排名，流量法宝
						</view>
					</view>
				</navigator>
			</view> -->
			<view class="spread-bottom">
				<navigator url="">
					<view class="img">
						<!-- <image src="../../static/img/images/images/mendian1.png" mode=""></image> -->
						<view class="iconfont icon-activity_icon"></view>
					</view>
					<view class="text">
						活动报名
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-xiaochengxutubiaoguilei1"></view>
					</view>
					<view class="text">
						门店装修
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-zhineng"></view>
					</view>
					<view class="text">
						智能满减
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-shuoshi"></view>
					</view>
					<view class="text">
						袋鼠学院
					</view>
				</navigator>
				
			</view>
			
		</view>
		<view class="classify">
			<view class="classify-top">
				配送服务
			</view>
			<view class="classify-bottom">
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-dianpingche"></view>
					</view>
					<view class="text">
						配送信息
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-icon-test"></view>
					</view>
					<view class="text">
						出餐时间
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-text-two"></view>
					</view>
					<view class="text">
						订单赔偿	
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-fuwushuoming"></view>
					</view>
					<view class="text">
						服务说明
					</view>
				</navigator>
			</view>
		</view>
		<view class="classify">
			<view class="classify-top">
				推荐服务
			</view>
			<view class="classify-bottom">
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-huiyuan-"></view>
					</view>
					<view class="text">
						美团会员
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-shequ1"></view>
					</view>
					<view class="text">
						商家社区
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-daishu"></view>
					</view>
					<view class="text">
						袋鼠店长
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-qrcode"></view>
					</view>
					<view class="text">
						二维码推广
					</view>
				</navigator>
			</view>
		</view>
		<view class="classify">
			<view class="classify-bottom">
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-menlingsiyinshejic"></view>
					</view>
					<view class="text">
						美团会员
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-zhongguohangtiantubiaoheji-weizhuanlunkuo-"></view>
					</view>
					<view class="text">
						快速出餐
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-renzheng"></view>
					</view>
					<view class="text">
						安全认证
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-dangao"></view>
					</view>
					<view class="text">
						二维码推广
					</view>
				</navigator>
			</view>
		</view>
		<view class="classify2">
			<view class="classify-bottom">
				<navigator url="../store-administration/store-administration">
					<view class="img">
						<view class="iconfont icon-shangpin"></view>
					</view>
					<view class="text">
						商品管理
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-guke-weixuan"></view>
					</view>
					<view class="text">
						顾客管理
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-duizhang"></view>
					</view>
					<view class="text">
						财务对账
					</view>
				</navigator>
				<navigator url="">
					<view class="img">
						<view class="iconfont icon-jingyingshujuicon"></view>
					</view>
					<view class="text">
						营运数据
					</view>
				</navigator>
			</view>
		</view>
		
	</view>
</template>
<script>
	export default {
		data() {
			return {
				
				}
		},
		methods: {
			
			}
	}
</script>

<style>
	.content {
		background-color: #f2f2f2;
		padding: 0;
		
	}
	.content .classify:nth-of-type(4) {
		margin-bottom: 0;
		padding-bottom: 5rpx;
		
	}
	.content .classify:nth-of-type(5) {
		padding-top: 0;
	}
	
	.top {
		display: flex;
		margin-bottom: 60rpx;
		margin-top: 30rpx;
		margin-bottom: 200rpx;
	}
	.top .top-item {
		flex: 1;
	}
	.top .top-item .number {
		text-align: center;
		font-size: 70rpx;
		font-weight: 100;
	}
	.top .top-item .number2 {
		text-align: center;
		font-size: 30rpx;
		color: #909092;
		
	}
	.spread {
		background-color: #FFFFFF;
		margin-bottom: 20rpx;
		padding: 40rpx;
		padding-top: 60rpx;
	}
	.spread .spread-top {
		display: flex;
	}
	.spread .spread-top navigator {
		flex: 1;
	}
	.spread .spread-top navigator .img {
		display: inline-block;
	}
	.spread .spread-top navigator .img image{
		width: 100rpx;
		height: 100rpx;
		display: inline-block;
	}
	.spread .spread-top navigator .text {
		display: inline-block;
		/* font-size: 15rpx; */
	}
	.spread .spread-top navigator .text .text1 {
		/* display: inline-block; */
		font-size: 40rpx;
		color: #6b6b6b;
	}
	.spread .spread-top navigator .text .text2 {
		/* display: inline-block; */
		font-size: 10rpx;
		color: #d0d0d0;
	}
	.spread .spread-bottom {
		display: flex;
	}
	.spread .spread-bottom navigator {
		flex: 1;
		text-align: center;
	}
	.spread .spread-bottom navigator .img .iconfont{
		font-size: 80rpx;
	}
	
	.spread .spread-bottom navigator {
		flex: 1;
	}
	.spread .spread-bottom navigator .img image {
		width: 100rpx;
		height: 100rpx;
	}
	.spread .spread-bottom navigator .text {
		color: #909092;
		font-size: 20rpx;
	}
	.classify {
		background-color: #FFFFFF;
		padding: 40rpx;
		margin-bottom: 30rpx;
	}
	.classify .classify-top {
		
	}
	.classify .classify-bottom {
		display: flex;
		margin-top: 20rpx;
	}
	.classify .classify-bottom navigator {
		flex: 1;
		text-align: center;
	}
	.classify .classify-bottom navigator .img .iconfont {
		font-size: 80rpx;
	}
	.classify .classify-bottom navigator .img image  {
		width: 120rpx;
		height: 120rpx;
	}
	.classify .classify-bottom navigator .text {
		color: #909092;
		font-size: 20rpx;
	}
	.classify2 {
		background-color: #FFFFFF;
		margin: 0 30rpx;
		padding: 40rpx;
		padding-top: 10rpx;
		position: absolute;
		top: 200rpx;
		left: 0;
		right: 0;
		box-shadow:0 0 1px #000 inset;
		
	}
	.classify2 .classify-top {
		
	}
	.classify2 .classify-bottom {
		display: flex;
		margin-top: 20rpx;
	}
	.classify2 .classify-bottom navigator {
		flex: 1;
		text-align: center;
	}
	.classify2 .classify-bottom navigator .img .iconfont {
		font-size: 80rpx;
	}
	.classify2 .classify-bottom navigator .text {
		color: #909092;
		font-size: 20rpx;
	}
</style>