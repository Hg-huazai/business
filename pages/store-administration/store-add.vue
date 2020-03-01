<template>
	<view class="content">
		<view class="content1">
			<view class="content1-top">
				基本信息
			</view>
			<form>
				<view class="box">
					<view class="item">
						<view class="left-l left">类型</view>
						<view class="left-l">
							<view>
								<label class="radio"><radio value="r1" :checked="curren==='r1'" @click="radio('r1')"/>单品</label>
								<label class="radio"><radio value="r2" :checked="curren==='r2'" @click="radio('r2')"/>套餐</label>
							</view>
						</view>
						<view class="clear"></view>
					</view>
					<view class="item">
						<view class="left-l left" >名称</view>
						<view class="left-l number">30秒以内</view>
						<view class="right-r voice">语音输入</view>
						<view class="clear"></view>
					</view>
					<view class="item">
						<view class="left-l left" >分类</view>
						<view class="left-l"><input type="text" value="" placeholder="打折扣, 煲仔粥" disabled="true" placeholder-style="font-weight: bold; font-size: 30rpx; color: #3a3843"/></view>
						<view class="right-r"><i class="iconfont icon-youjiantou"></i></view>
						<view class="clear"></view>
					</view>
					<view class="item none">
						<view class="left-l left">图片</view>
						<view class="left-l right">
							<view class="img1">
								<view class="left-l">可以给图片"打光标啦",突出菜品买点，提高销量新玩法~</view>
								<view class="right-r">查看详情<i class="iconfont icon-youjiantou"></i></view>
								<view class="clear"></view>
							</view>
							<view class="img2">
								<!-- <image src="../../static/img/images/0ec2a489ee414e19c6cde9efbaa15c5_03.png" mode="widthFix"></image> -->
								<i class="iconfont icon-jiahao"></i>
							</view>
							<view class="img3">
								<view class="left-l">图片需要大于600x450像素</view>
								<view class="right-r">图片规范<i class="iconfont icon-youjiantou"></i></view>
								<view class="clear"></view>
							</view>
							<view class="img4">
								<view class="left-l">为什么用真实的图片后,商品销量会更高?</view>
								<view class="clear"></view>
							</view>
						</view>
						<view class="clear"></view>
					</view>
				</view>
			</form>
		</view>
		<view class="content2">
			<view class="content2-top">
				<view class="left-l">详细信息</view>
				<view class="right-r">查看示例</view>
				<view class="clear"></view>
			</view>
			<view class="box">
				<view class="item">
					<view class="left-l left">标签</view>
					<view class="left-l right">
						<view class="top">添加标签</view>
						<view class="bottom">如商品菜系、主料、配料等</view>
					</view>
					<view class="clear"></view>
				</view>
				<view class="item">
					<view class="left-l left">属性</view>
					<view class="left-l right">
						<view class="top">添加属性</view>
						<view class="bottom">下单时多种口味、如加糖/无糖、微辣/免辣</view>
					</view>
					<view class="clear"></view>
				</view>
				<view class="item none">
					<view class="left-l left">描述</view>
					<view class="left-l right">
						<textarea value="" placeholder="200字以内,请输入" placeholder-style="color: #bababa;" auto-height="true" />
					</view>
					<view class="clear"></view>
				</view>
			</view>
		</view>
		<view class="content3">
			<view class="content3-top1">
				<view class="left-l"><i class="iconfont icon-tanhao1" style="color: #929395;"></i>店铺页商品详细信息可自定义设置哦~</view>
				<view class="right-r">预览与设置<i class="iconfont icon-youjiantou"></i></view>
				<view class="clear"></view>
			</view>
			<view class="content3-top2">
				<view class="left-l">售卖信息</view>
				<view class="right-r right">查看示例</view>
				<view class="clear"></view>
			</view>
			<view class="box">
				<view class="item none">
					<view class="left-l left">规格</view>
					<view class="left-l right">
						<view class="top">设置价格和库存</view>
					</view>
					<view class="clear"></view>
				</view>
			</view>
			<view class="content3-top3">
				<view class="left-l">高级信息</view>
				<view class="right-r right">展开<i class="iconfont icon-youjiantou-copy"></i></view>
				<view class="clear"></view>
			</view>
			<view class="box">
				<view class="item">
					<view class="left-l">可售时间，商品单位，商品特色，最少购买等</view>
					<view class="clear"></view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data(){
			return {
				curren: 'r1'
			}
		},
		methods: {
			radio(e) {
				this.curren = e;
				console.log(e);
			}
		}
	}
	
	
</script>

<style>
	.left-l {
		float: left;
	}
	.right-r {
		float: right;
	}
	.clear {
		clear: both;
	}
	.content {
		padding: 0;
	}
	.content1 .content1-top {
		background-color: #f2f2f2;
		color: #898989;
		padding: 40rpx 0 20rpx 30rpx;
		font-size: 28rpx;
	}
	.content1 .box {
		background-color: #FFFFFF;
		width: 100%;
		padding: 0 30rpx;
		box-sizing: border-box;
		font-size: 30rpx;
		border-bottom: 2rpx solid #ebebeb;
	}
	.content1 .box .item{
		padding: 30rpx 0;
		border-bottom: 2rpx solid #ebebeb;
	}
	.content1 .box .item.none{
		border-bottom: none;
	}
	.content1 .box .left-l.left{
		width: 20%;
		color: #2c2c2a;
	}
	.content1 .box .left-l.right{
		width: 80%;
	}
	.content1 .box .left-l .radio {
		font-weight: bold;
		margin-right: 15rpx;
		color: #3a3843
	}
	.content1 .box .left-l.number {
		color: #9b9b9b;
	}
	.content1 .box .right-r.voice {
		color: #343434;
		padding-left: 30rpx;
		border-left: 2rpx solid #ebebeb;
	}
	.content1 .box .right-r .iconfont {
		font-size: 26rpx;
		color: #999999;
	}
	.content1 .box .left-l.right .img1{
		border: 2rpx solid #dbdbdb;
		color: #838383;
		padding: 10rpx 20rpx;
	}
	.content1 .box .left-l.right .img1 .left-l{
		width: 85%;
	}
	.content1 .box .left-l.right .img1 .right-r{
		color: #d4993b;
	}
	.content1 .box .left-l.right .img1 .right-r .iconfont{
		font-size: 20rpx;
		margin-left: 10rpx;
	}
	.content1 .box .left-l.right .img2{
		width: 200rpx;
		height: 150rpx;
		background-color: #e7e6ec;
		margin-top: 20rpx;
		overflow: hidden;
		text-align: center;
		line-height: 150rpx;
	}
	.content1 .box .left-l.right .img2 .iconfont{
		font-size: 80rpx;
		color: #95949c;
	}
	.content1 .box .left-l.right .img2 image{
		width: 200rpx;
	}
	.content1 .box .left-l.right .img3{
		margin-top: 20rpx;
		font-size: 26rpx;
	}
	.content1 .box .left-l.right .img3 .left-l {
		color: #9c9ba1;
	}
	.content1 .box .left-l.right .img3 .right-r {
		color: #d4993b;
	}
	.content1 .box .left-l.right .img3 .right-r .iconfont{
		font-size: 20rpx;
		margin-left: 8rpx;
	}
	.content1 .box .left-l.right .img4{
		font-size: 26rpx;
		color: #d4993b;
		margin-top: 20rpx;
	}
	
	.content2 .content2-top {
		background-color: #f2f2f2;
		color: #898989;
		padding: 40rpx 30rpx 20rpx 30rpx;
		font-size: 28rpx;
	}
	.content2 .content2-top .right-r {
		color: #3c3c3e;
		font-size: 18rpx;
		border: 2rpx solid #bbbbbb;
		padding: 6rpx 10rpx;
	}
	.content2 .box {
		background-color: #FFFFFF;
		width: 100%;
		padding: 0 30rpx;
		box-sizing: border-box;
		font-size: 30rpx;
		border-bottom: 2rpx solid #ebebeb;
	}
	.content2 .box .left-l.left{
		width: 20%;
		color: #3e3d43;
	}
	.content2 .box .left-l.right{
		width: 80%;
	}
	.content2 .box .left-l.right .top{
		color: #d69c17;
	}
	.content2 .box .left-l.right .bottom{
		color: #808080;
		font-size: 30rpx;
		margin-top: 5rpx;
	}
	.content2 .box .left-l.right textarea {
		width: 98%;
	}
	.content2 .box .item{
		padding: 30rpx 0;
		border-bottom: 2rpx solid #ebebeb;
	}
	.content2 .box .item.none{
		border-bottom: none;
	}
	
	.content3 .content3-top1 {
		background-color: #fffaf2;
		color: #898989;
		padding: 40rpx 30rpx 20rpx 30rpx;
		font-size: 28rpx;
	}
	.content3 .content3-top1 .right-r {
		color: #41403e;
		font-size: 27rpx;
	}
	.content3 .content3-top1 .left-l {
		color: #9f9f9f;
		font-size: 26rpx;
	}
	.content3 .content3-top1 .left-l .iconfont {
		color: #9f9f9f;
		font-size: 28rpx;
		margin-right: 10rpx;
	}
	.content3 .content3-top1 .right-r .iconfont {
		color: #8c8d85;
		font-size: 20rpx;
		margin-left: 10rpx;
	}

	.content3 .content3-top2 {
		background-color: #f2f2f2;
		color: #898989;
		padding: 40rpx 30rpx 20rpx 30rpx;
		font-size: 28rpx;
	}
	.content3 .content3-top2 .right-r {
		color: #3c3c3e;
		font-size: 18rpx;
		border: 2rpx solid #bbbbbb;
		padding: 6rpx 10rpx;
	}
	.content3 .content3-top3 {
		background-color: #f2f2f2;
		color: #898989;
		padding: 40rpx 30rpx 20rpx 30rpx;
		font-size: 28rpx;
	}
	.content3 .content3-top3 .right-r {
		color: #3c3c3e;
		font-size: 28rpx;
	}
	.content3 .content3-top3 .right-r .iconfont {
		font-size: 5px;
		margin-left: 10rpx;
	}
	.content3 .box {
		background-color: #FFFFFF;
		width: 100%;
		padding: 0 30rpx;
		box-sizing: border-box;
		font-size: 30rpx;
		border-bottom: 2rpx solid #ebebeb;
	}
	.content3 .box .item{
		padding: 30rpx 0;
		border-bottom: 2rpx solid #ebebeb;
	}
	.content3 .box .item.none{
		border-bottom: none;
	}
	.content3 .box .left-l.left{
		width: 20%;
		color: #3e3d43;
	}
	.content3 .box .left-l.right{
		width: 80%;
	}
	.content3 .box .left-l.right .top{
		color: #d69c17;
	}
</style>
