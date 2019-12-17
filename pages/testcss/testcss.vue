<template>
	<view>
		<!-- 使用动画库 -->
		<view class="box animated bounce"></view>
		<!-- 使用图标 -->
		<view class="icon iconfont icon-shengdanjie-lingdang"></view>
		
		<!-- css 数据绑定 -->
		<!-- <view class="box" :class="[box1, box2]"></view> -->
		<view class="box" :class="[age > 10 ? box1:'' , box2]"></view>
		<view :class="{'class1':isActive}"></view>
		
		<!-- css样式变量 -->
		<!-- <view class="box" :style="{height: height + 'rpx'}"></view> -->
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				height:400,
				age:3,
				box1:"class1",
				box2:"class2",
				isActive:true
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	/* 引入动画css */
	@import url("../../common/animate.css");	
	/* 引入阿里图标svg css */
	@import url("../../common/iconfont.css");	
	
	.box{
		width: 200rpx;
		height: 200rpx;
		background: #4CD964;
	}
	
	.class1{
		width: 400rpx;
		height: 500rpx;
		border: 1rpx solid #333333;
	}
	.class2{
		background: #007AFF;
	}
</style>
