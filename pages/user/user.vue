<template>
	<view class="content">
		<view class="info">
			<view class="info-left">
				<view class="img">
					<image src="../../static/img/images/0ec2a489ee414e19c6cde9efbaa15c5_03.png" mode=""></image>
				</view>
				<view class="info-item">
					<view class="info-name">
						蒙骨煲粥(百信店)
					</view>
					<view class="info-work">
						<view class="dian"></view>
						<text> &nbsp;营业中 &gt;</text>
					</view>
				</view>
			</view>
			<view class="info-right">
				&gt;
			</view>
		</view>
		<view class="wellet">
			<view class="wellet-top">
				<view class="money">我的钱包</view>
				<navigator url="">进入钱包 &gt;</navigator>
			</view>
			<view class="wellet-bottom">
				<view class="wellet-bottom-item">
					<view class="wellet-bottom-item1">
						账号管理
					</view>
					<view class="wellet-bottom-item2">
						<text>1</text>张
					</view>
					<view class="wellet-bottom-item1">
						银行卡
					</view>
				</view>
				<view class="wellet-bottom-item">
					<view class="wellet-bottom-item1">
						生意贷(元)
					</view>
					<view class="wellet-bottom-item2">
						<text>100</text>万
					</view>
					<view class="wellet-bottom-item1">
						最高额度
					</view>
				</view>
				<view class="wellet-bottom-item">
					<view class="wellet-bottom-item1">
						生意宝
					</view>
					<view class="wellet-bottom-item2">
						<text>3.0</text>%
					</view>
					<view class="wellet-bottom-item1">
						天天赚
					</view>
				</view>
			</view>
		</view>
		<view class="set-up">
			<navigator url="../set-up/set-up">
				<image src="../../static/img/images/images/classify_09.png" mode=""></image>
				<view class='text'>门店设置</view>
			</navigator>
			<navigator>
				<image src="../../static/img/images/images/classify_09.png" mode=""></image>
				<view class='text'>订单设置</view>
			</navigator>
			<navigator>
				<image src="../../static/img/images/images/classify_09.png" mode=""></image>
				<view class='text'>打印设置</view>
			</navigator>
			<navigator>
				<image src="../../static/img/images/images/classify_09.png" mode=""></image>
				<view class='text'>消息和铃声</view>
			</navigator>
		</view>
		
		<view class="service">
			<ul>
				<li>
					<navigator>
						<text class="service-left">联系业务经理</text>
						<text class="service-right">&gt;</text>
					</navigator>
				</li>
				<li>
					<navigator>
						<text class="service-left">商家服务中心</text>
						<text class="service-right">&gt;</text>
					</navigator>
				</li>
				<li>
					<navigator>
						<text class="service-left">意见反馈</text>
						<text class="service-right">&gt;</text>
					</navigator>
				</li>
			</ul>
		</view>
		<view class="service">
			<ul>
				<li>
					<navigator>
						<text class="service-left">当前账号</text>
						<text class="service-right">&gt;</text>
						<text class="new">6677876665</text>
					</navigator>
				</li>
				<li>
					<navigator>
						<text class="service-left">检查版本更新</text>
						<text class="service-right">&gt;</text>
					</navigator>
				</li>
			</ul>
		</view>
		<view class="btn-row">
			<button v-if="!hasLogin" type="primary" class="primary" @tap="bindLogin">登录</button>
			<button v-if="hasLogin" type="default" @tap="bindLogout">退出登录</button>
		</view>
	</view>
</template>

<script>
	import {
		mapState,
		mapMutations
	} from 'vuex'

	export default {
		computed: {
			...mapState(['hasLogin', 'forcedLogin'])
		},
		methods: {
			...mapMutations(['logout']),
			bindLogin() {
				uni.navigateTo({
					url: '../login/login',
				});
			},
			bindLogout() {
				this.logout();
				/**
				 * 如果需要强制登录跳转回登录页面
				 */
				if (this.forcedLogin) {
					uni.reLaunch({
						url: '../login/login',
					});
				}
			}
		}
	}
</script>

<style>
	.info {
		margin: 40rpx 0;
		/* background-color: pink; */
		
	}
	.info .info-left {
		float: left;
		
	}
	.info .info-left .img {
		float: left;
	}
	.info .info-left image {
		width: 140rpx;
		height: 140rpx;
		display: inline-block;
		
		
	}
	.info .info-left .info-item {
		display: inline-block;
		margin-left: 25rpx;
	}
	.info .info-left .info-item .info-name {
		font-size: 40rpx;
		margin-top: 10rpx;
		margin-bottom: 10rpx;
	}
	.info .info-left .info-item .info-work {
		background-color: #eae8e9;
		display: inline;
		padding: 2rpx 15rpx;
	}
	.info .info-left .info-item .info-work .dian {
		display: inline-block;
		width: 20rpx;
		height: 20rpx;
		border-radius: 50%;
		background-color: #1fc57b;
	}
	.info .info-right {
		float:right;
		margin-top: 55rpx;
		padding-right: 20rpx;
		color: #c7c5d2;
	}
	.wellet {
		background-color: #FFFFFF;
		width: 100%;
		padding: 40rpx 40rpx;
		box-sizing: border-box;
	}
	.wellet .wellet-top {
		width: 100%;
	}
	.wellet .money {
		display: inline-block;
	}
		
	.wellet navigator {
		display: inline-block;
		float: right;
		font-size: 16rpx;
	}
	.wellet .wellet-bottom {
		display: flex;
		margin-top: 40rpx;
		justify-content: space-between;
	}
	
	.wellet .wellet-bottom .wellet-bottom-item {
		/* justify-content: center; */
		/* flex: 1; */
	}
	.wellet .wellet-bottom .wellet-bottom-item .wellet-bottom-item1 {
		font-size: 16rpx;
		margin: 0 auto;
		color: #9f9fa1;
	}
	.wellet .wellet-bottom .wellet-bottom-item .wellet-bottom-item2 {
		font-size: 8rpx;
		margin: 0 auto;
		color: #9f9fa1;
	}
	.wellet .wellet-bottom .wellet-bottom-item .wellet-bottom-item2 text {
		font-size: 50rpx;
		color: #000000;
	}
	.set-up {
		background-color: #FFFFFF;
		margin-top: 20rpx;
		display: flex;
		justify-content: space-between;
		width: 100%;
	}
	.set-up navigator {
		flex: 1;
		border-right: 1px solid #8F8F94;
		padding: 20px 0;
	}
	.set-up navigator:last-child {
		border-right: none;
	}
	.set-up navigator image {
		height: 100rpx;
		width: 100rpx;
		margin-left: 40rpx;
	}
	.set-up navigator .text {
		font-size: 18rpx;
		/* display: inline-block; */
		width: 100%;
		text-align: center;
		margin: 0 auto;
	}
	.service {
		background-color: #FFFFFF;
		margin-top: 20rpx;
	}
	.service ul {
		padding-left: 0;
	}
	.service li {
		list-style: none;
		height: 100rpx;
		line-height: 100rpx;
		border-bottom: 1px solid #989898;
		padding: 0 18rpx;
		
	}
	.service li:last-child {
		border-bottom: none;
	}
	.service li navigator {
		display: inline-block;
		width: 100%;
		height: 100%;
		
	}
	.service li navigator .service-left {
		
	}
	.service li navigator .service-right {
		float: right;
	}
	.service li navigator .new {
		float: right;
		font-size: 18rpx;
	}
</style>
