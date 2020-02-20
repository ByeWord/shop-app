<template>
	<view class="card">
		<view class="card-header">
			<view>-</view>
			<slot>
				<view class="card-title">{{title}}</view>
			</slot>
			<view>-</view>
		</view>
	</view>
</template>

<script>
	export default{
		name:'Card',
		props:{
			title:{
				type:String,
				default:""
			}
		}
	}
</script>

<style scoped>
	.card{
		display: flex;
		flex-direction: column;
	}
	.card-header{
		display: flex;
		justify-content: center;
		align-items: center;
		padding: 0 30rpx;
		font-size: 32rpx;
		font-weight: bold;
	}
	.card-title{
		padding: 0 20rpx;
	}
</style>
