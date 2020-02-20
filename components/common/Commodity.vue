<template>
	<view class="commodity" :style="[shouldWrap]">
		<view class="commodity-item" :style="[itemW]" v-for="item in dataList" :key="item.id">
			<image class="commodity-img" :src="item.imgSrc" mode="widthFix"></image>
			<view class="text-message">
				<text class="commodity-description">{{item.description}}</text>
				<view>
					<text class="cprice">￥{{item.cprice}}</text>
					<text class="oprice">￥{{item.oprice}}</text>
				</view>
				<text class="discount">{{item.discount}}折</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "Commodity",
		props: {
			colCount: {
				type: Number | Number,
				default: 2,
				validator: (v) => Number.isInteger(Number(v))
			},
			wrap: {
				type: Boolean,
				default: true
			},
			colW: {
				type: String | Number,
				default: ''
			},
			dataList: {
				type: Array,
				default: () => []
			}
		},
		computed: {
			itemW() {
				if (this.colW) {
					return {
						width: `${this.colW}rpx`
					}
				} else {
					return {
						width: `${100 / Number(this.colCount)}%`
					}
				}
			},
			shouldWrap() {
				return this.wrap ? {
					flexWrap: 'wrap'
				} : ''
			}
		},
		methods: {

		}
	}
</script>

<style scoped>
	.commodity {
		display: flex;
	}

	.commodity-item {
		box-sizing: border-box;
		flex-shrink: 0;
	}

	.commodity-img {
		width: 100%;
	}

	.text-message {
		text-align: center;
	}

	.commodity-description {
		text-align: center;
		overflow: hidden;
		text-overflow: ellipsis;
		display: -webkit-box;
		-webkit-line-clamp: 2;
		-webkit-box-orient: vertical;
		word-break: break-all;
		color: #333333;
		line-height: 1.2;
		font-size: 24rpx;
	}

	image {
		will-change: transform
	}

	.oprice,
	.cprice {
		font-size: 20rpx;
	}

	.oprice {
		color: #CCCCCC;
		text-decoration: line-through;
		margin-left: 4rpx;
	}

	.discount {
		color: #FF3333;
		border: 1px solid #FF3333;
		font-size: 20rpx;
		padding: 2rpx 4rpx;
		border-radius: 4rpx;
	}
</style>
