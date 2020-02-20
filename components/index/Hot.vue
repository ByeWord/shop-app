<template>
	<view class="hot">
		<Commodity :col-count="3" :dataList="dataList"></Commodity>
	</view>
</template>

<script>
	import Commodity from '@/components/common/Commodity.vue';
	export default {
		name: 'Hot',
		components: {
			Commodity
		},
		data() {
			return {
				dataList: [{
					id: 1,
					description: '热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款',
					oprice:'399',
					cprice:'255',
					discount:'5.5',
					imgSrc:'../../static/images/hot1.jpg'
				},
				{
					id: 2,
					description: '热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款',
					oprice:'399',
					cprice:'255',
					discount:'5.5',
					imgSrc:'../../static/images/hot2.jpg'
				},
				{
					id: 3,
					description: '热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款热卖爆款',
					oprice:'399',
					cprice:'255',
					discount:'5.5',
					imgSrc:'../../static/images/hot3.jpg'
				}]
			}
		}
	}
</script>

<style>
</style>
