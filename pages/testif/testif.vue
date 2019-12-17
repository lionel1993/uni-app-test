<template>
	<view>
		
		 <view v-if="is_show">
			哈哈哈哈哈哈哈哈哈
		</view>
		<view v-else>aaa</view>
		
		<view v-if="age > 30">
			显示区域1
		</view>
		<view v-else-if="age > 20">
			显示区域2
		</view>
		<view v-else>
			显示区域3		
		</view>
	
	</view>
</template>

<script>
	export default {
		data() {
			return {
				is_show: false,
				age : 23
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
