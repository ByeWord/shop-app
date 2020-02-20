<template>
	<view class="shop">
		<Card title="店铺推荐"></Card>
		<Banner imgSrc="../../static/images/shop.jpg"></Banner>
		<scroll-view scroll-x class="scroll-content">
			<view class="scroll-item">
				<Commodity :dataList="shopList" :wrap="false" colW="200"></Commodity>
			</view>
		</scroll-view>
	</view>
</template>

<script>
	import Banner from '@/components/index/Banner.vue';
	import Card from '@/components/common/Card.vue';
	import Commodity from '@/components/common/Commodity.vue';
	export default{
		name:"Shop",
		components:{
			Banner,
			Card,
			Commodity
		},
		data(){
			return{
				shopList:[
					{
						id: 1,
						description: '塞尔达',
						oprice:'399',
						cprice:'255',
						discount:'5.5',
						imgSrc:'../../static/images/shop1.jpg'
					},
					{
						id: 2,
						description: '口袋妖怪',
						oprice:'399',
						cprice:'255',
						discount:'5.5',
						imgSrc:'../../static/images/shop2.jpg'
					},
					{
						id: 3,
						description: '火焰纹章',
						oprice:'399',
						cprice:'255',
						discount:'5.5',
						imgSrc:'../../static/images/shop3.jpg'
					},
					{
						id: 4,
						description: '异度之刃',
						oprice:'399',
						cprice:'255',
						discount:'5.5',
						imgSrc:'../../static/images/shop4.jpg'
					}
				]
			}
		}
	}
</script>

<style>
</style>
