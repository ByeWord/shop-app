<template>
	<view class="content">
		<scroll-view 
			:scroll-x="true" 
			@scrolltolower="onScrolltolower" 
			@scroll="onScroll"
			class="scroll-content"
			:scroll-into-view="scrollIntoView"
		>
			<view 
				v-for="(item,index) in topBar" 
				class="scroll-item" 
				@click="onNavItemClick(index)" :key="item.id"
				:id="`item_${index}`"
			 >
				<text 
					:class="[activeIndex === index?'f-active-color':'']"
					>
					{{item.title}}
				</text>
			</view>
		</scroll-view>
		<swiper @change='onSwiperChange' :current="activeIndex">
			<swiper-item v-for="(item,index) in topBar" :key='item.id'>
				<view class="swiper-item">{{item.title}}</view>
			</swiper-item>
		</swiper>
		<!-- 	<IndexSwiper></IndexSwiper>
		<IndexRecomnend></IndexRecomnend>
		<Card></Card>
		<CommodityList></CommodityList> -->
		<Banner imgSrc="../../static/images/banner1.jpg"></Banner>
		<Icons></Icons>
		<Hot></Hot>
		<Shop></Shop>
	</view>
</template>

<script>
	import IndexSwiper from '@/components/index/IndexSwiper.vue';
	import IndexRecomnend from '@/components/index/Recommend.vue'
	import Card from '@/components/common/Card.vue';
	import CommodityList from '@/components/common/CommodityList.vue';
	import Banner from '@/components/index/Banner.vue';
	import Icons from '@/components/index/Icons.vue';
	import Hot from '@/components/index/Hot.vue';
	import Shop from '@/components/index/Shop.vue';
	export default {
		data() {
			return {
				title: 'Hello',
				activeIndex: 0,
				topBar: [{
						id: 1,
						title: '推荐'
					},
					{
						id: 2,
						title: '运动户外'
					},
					{
						id: 3,
						title: '服饰内衣'
					},
					{
						id: 4,
						title: '鞋靴箱包'
					},
					{
						id: 5,
						title: '美妆个护'
					},
					{
						id: 6,
						title: '家具数码'
					},
					{
						id: 7,
						title: '视频母婴'
					}
				]
			}
		},
		computed:{
			scrollIntoView(){
				return `item_${this.activeIndex}`
			}
		},
		components: {
			IndexSwiper,
			IndexRecomnend,
			Card,
			CommodityList,
			Banner,
			Icons,
			Hot,
			Shop
		},
		onLoad() {

		},
		methods: {
			onScrolltolower(arg) {
				// console.log('onScrolltolower',arg)
			},
			onScroll(event) {
				// console.log(event)
			},
			onNavItemClick(index) {
				this.activeIndex = Number(index);
			},
			onSwiperChange(event){
				this.activeIndex = event.detail.current
			}
		}
	}
</script>

<style scoped>
	.scroll-content {
		width: 100%;
		white-space: nowrap;
	}

	.scroll-item {
		display: inline-block;
		padding: 10rpx 30rpx;
		font-size: 32rpx;
		white-space: nowrap;
	}
	.scroll-item .f-active-color{
		padding: 10rpx 0;
		border-bottom: 4rpx solid #49BDFB;
	}
</style>
