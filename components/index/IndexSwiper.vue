<template>
	<view class="swiper-wrapper">
		<swiper indicator-dots>
			<swiper-item>
				<view>
					<image class="swiper-image" src="../../static/images/swiper1.jpg" mode="aspectFill"></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view>
					<image class="swiper-image" src="../../static/images/swiper2.jpg" mode="aspectFill"></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view>
					<image class="swiper-image" src="../../static/images/swiper3.jpg" mode="aspectFill"></image>
				</view>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default{
		name:"IndexSwiper"
	}
</script>

<style scoped>
	swiper{
		width: 100%;
		height: 320rpx;
	}
	.swiper-image{
		width: 100%;
		height: 320rpx;
	}
</style>
