<template>
	<view class="content">
		<view class="service">
			<ul>
				<li>
					<navigator>
						<text class="service-left">门店名称</text>
						<text class="service-right iconfont icon-youjiantou"></text>
						<text class="new">蒙骨煲粥(百信店)</text>
					</navigator>
				</li>
				<li>
					<navigator>
						<text class="service-left">营运品类</text>
						<text class="service-right iconfont icon-youjiantou"></text>
						<text class="new">美食-快餐-包子/粥</text>
					</navigator>
				</li>
				<li class="active active1">
					<navigator>
						<text class="service-left">店铺头像</text>
						<text class="service-right iconfont icon-youjiantou"></text>
						<view class="new1">
							<image src="../../static/img/images/0ec2a489ee414e19c6cde9efbaa15c5_03.png" mode="widthFix"></image>
						</view>
					</navigator>
				</li>
			</ul>
		</view>
		<view class="service">
			<ul>
				<li>
					<navigator>
						<text class="service-left">营业状态</text>
						<text class="service-right iconfont icon-youjiantou"></text>
						<text class="new">营业中</text>
					</navigator>
				</li>
				<li>
					<navigator>
						<text class="service-left">歇业保护</text>
						<text class="service-right iconfont icon-youjiantou"></text>
						<text class="new">未设置</text>
					</navigator>
				</li>
				<li>
					<navigator>
						<text class="service-left">门店公告</text>
						<text class="service-right iconfont icon-youjiantou"></text>
						<text class="new">新店钜惠，大额满减</text>
					</navigator>
				</li>
				<li>
					<navigator>
						<text class="service-left">餐厅电话</text>
						<text class="service-right iconfont icon-youjiantou"></text>
						<text class="new">13902275382</text>
					</navigator>
				</li>
				<li>
					<navigator>
						<text class="service-left">餐厅地址</text>
						<text class="service-right iconfont icon-youjiantou"></text>
						<text class="new">新市街四巷8号101房</text>
					</navigator>
				</li>
				<li>
					<navigator>
						<text class="service-left">营业时间</text>
						<text class="service-right iconfont icon-youjiantou"></text>
						<text class="new">00:00-03:00 07:20-23:59</text>
					</navigator>
				</li>
				<li class="active">
					<navigator>
						<text class="service-left">青山公益行动</text>
						<text class="service-right iconfont icon-youjiantou"></text>
						<text class="new">一起助力环保</text>
					</navigator>
				</li>
			</ul>
		</view>
		<view class="service">
			<ul>
				<li>
					<navigator>
						<text class="service-left">费率查询</text>
						<text class="service-right iconfont icon-youjiantou"></text>
						<text class="new"></text>
					</navigator>
				</li>
				<li>
					<navigator>
						<text class="service-left">营业资质</text>
						<text class="service-right iconfont icon-youjiantou"></text>
						<text class="new"></text>
					</navigator>
				</li>
				<li class="active">
					<navigator>
						<text class="service-left">电子合同</text>
						<text class="service-right iconfont icon-youjiantou"></text>
						<text class="new">生效中</text>
					</navigator>
				</li>
			</ul>
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
		padding: 0;
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
		border-bottom: 2rpx solid #eaeaea;
		padding: 0 18rpx;
	}
	.service li.active {
		height: 150rpx;
		line-height: 150rpx;
	}
	.service .active {
		border-bottom: 0;
	}
	.service li navigator {
		display: inline-block;
		width: 100%;
		height: 100%;
		
	}
	.service li navigator .service-left {
		color: #696969;
		font-size: 15px;
	}
	
	.service li navigator .service-right {
		float: right;
		color: #b9b9b9;
		font-size: 25rpx;
		margin-left: 10rpx;
	}
	.service li navigator .new {
		float: right;
		font-size: 25rpx;
		color: #b9b9b9;
	}
	.service li navigator .new1 {
		float: right;
		margin-top: 25rpx;
	}
	.service li navigator .new1 image{
		width: 100rpx;
	}
</style>
