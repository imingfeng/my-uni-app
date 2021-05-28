<template>
	<view class="container">
		<!-- <uni-search-bar v-model="keywords" @confirm="search" /> -->
		<view>
			<z-calendar 
				:datePrice="datePrice" 
				howManyMonth="6" 
				@changeDate="changeDate" 
				defaultSelect="2021-05-28"
				mode="1">
			</z-calendar>
		</view>
	</view>
</template>

<script>
	import icon from '@/static/logo.png'
	import zCalendar from "@/components/calendar/index.vue"
	export default {
		data() {
			return {
				icon,
				keywords: '',
				datePrice: [{
						date: "2021-05-14",
						price: "111",
						endNum: 10
					},
					{
						date: "2021-05-24",
						price: "333",
						endNum: 5
					},
				]
			}
		},
		methods: {
			changeDate(data) {
				console.log(data)
			}
		},
		components: {
			zCalendar
		}
	}
</script>

<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
</style>
