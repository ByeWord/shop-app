<template>
	<view class="recommend bg-color">
		<view class="container">
			<image class="image-lg" src="../../static/images/Children.jpg" mode="aspectFill"></image>
			<view class="sub-images">
				<image class="image-sm" src="../../static/images/Children1.jpg" mode="aspectFill"></image>
				<image class="image-sm" src="../../static/images/Children2.jpg" mode="aspectFill"></image>
				<image class="image-sm" src="../../static/images/Children3.jpg" mode="aspectFill"></image>
			</view>
		</view>
		<view class="container">
			<image class="image-lg" src="../../static/images/Furnishing.jpg" mode="aspectFill"></image>
			<view class="sub-images">
				<image class="image-sm" src="../../static/images/Furnishing1.jpg" mode="aspectFill"></image>
				<image class="image-sm" src="../../static/images/Furnishing2.jpg" mode="aspectFill"></image>
				<image class="image-sm" src="../../static/images/Furnishing3.jpg" mode="aspectFill"></image>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: 'Recommend'
	}
</script>

<style scoped>
	.recommend{
		padding: 20rpx;
	}
	.container {
		border-radius: 20rpx;
		overflow: hidden;
	}
		
	.container:not(:first-child){
		margin-top: 20rpx;
	}
	image {
		display: block;
	}

	.image-lg {
		width: 100%;
		height: 280rpx;
	}
	.sub-images{
		display: flex;
	}
	.image-sm{
		flex: 33.3333%;
		height: 240rpx;
	}
</style>
