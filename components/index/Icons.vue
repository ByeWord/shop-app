<template>
	<view class="icons">
		<view class="icon-item">
			<image class="icon-img" src="../../static/images/icons1.png" mode="widthFix"></image>
			<text class="f-color">奢侈品</text>
		</view>
		<view class="icon-item">
			<image class="icon-img" src="../../static/images/icons1.png" mode="widthFix"></image>
			<text class="f-color">奢侈品</text>
		</view>
		<view class="icon-item">
			<image class="icon-img" src="../../static/images/icons1.png" mode="widthFix"></image>
			<text class="f-color">奢侈品</text>
		</view>
		<view class="icon-item">
			<image class="icon-img" src="../../static/images/icons1.png" mode="widthFix"></image>
			<text class="f-color">奢侈品</text>
		</view>
		<view class="icon-item">
			<image class="icon-img" src="../../static/images/icons1.png" mode="widthFix"></image>
			<text class="f-color">奢侈品</text>
		</view>
		<view class="icon-item">
			<image class="icon-img" src="../../static/images/icons1.png" mode="widthFix"></image>
			<text class="f-color">奢侈品</text>
		</view>
		<view class="icon-item">
			<image class="icon-img" src="../../static/images/icons1.png" mode="widthFix"></image>
			<text class="f-color">奢侈品</text>
		</view>
		<view class="icon-item">
			<image class="icon-img" src="../../static/images/icons1.png" mode="widthFix"></image>
			<text class="f-color">奢侈品</text>
		</view>
	</view>
</template>

<script>
	export default{
		name:"Icons"
	}
</script>

<style scoped>
	.icons{
		display: flex;
		flex-wrap: wrap;
	}
	.icon-item{
		width: 25%;
		display: flex;
		flex-direction: column;
		align-items: center;
		padding-top: 20rpx;
	}
	.icon-img{
		width: 100rpx;
	}
	.f-color{
		font-size: 24rpx;
	}
</style>
