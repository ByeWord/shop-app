<template>
	<view class="banner">
		<image class="banner-img" :src="imgSrc" mode="widthFix"></image>
	</view>
</template>

<script>
	export default{
		props:{
			imgSrc:{
				type:String,
				default:""
			}
		}
	}
</script>

<style scoped>
	.banner-img{
		width: 100%;
		display: block;
	}
</style>