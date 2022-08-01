<template>
	<view class="content">
		<view class="tab">
			<u-tabs :list="list1" @click="click" class="w" :scrollable="false"></u-tabs>
		</view>
		<view class="view">
			<Home v-if="index===0"></Home>
			<News v-if="index===1"></News>
			<Count v-if="index===2"></Count>
			<Price v-if="index===3"></Price>
			<Price v-if="index===4"></Price>
			<Price v-if="index===5"></Price>
			<Price v-if="index===6"></Price>
		</view>
	</view>
</template>

<script>
	import Home from "@/components/Home/Home.vue"
	import Free from "@/components/Free/Free.vue"
	import Practical from "@/components/Practical/Practical.vue"
	import System from "@/components/System/System.vue"
	import Column from "@/components/Column/Column.vue"
	import Note from "@/components/Note/Note.vue"
	import Mooc from "@/components/Mooc/Mooc.vue"
	
	export default {
		data() {
			return {
				list1:[
					{name:"首页"},
					{name:"免费课"},
					{name:"实战课"},
					{name:"体系课"},
					{name:"专栏"},
					{name:"手记"},
					{name:"慕课教程"},
				],
				arrs:["Home","Free","Practical","System","Column","Note","Mooc"],
				iscomponent:"Practical",
				practical:true,
				news:false,
				count:false,
				index: 4
			}
		},
		components:{
			Home,
			Free,
			Peactical,
			System,
			Column,
			Note,
			Mooc,
		},
		onLoad() {

		},
		methods: {
			click(item){
				this.index=item.index
			}
		}
	}
</script>

<style lang="scss">
	
</style>
