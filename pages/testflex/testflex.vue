<template>
	<view>
		<view class="box">
			<view class="box-item">1</view>
			<view class="box-item">2</view>
			<view class="box-item">3</view>
			<view class="box-item">4</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.box{
		width: 100%;
		height: 600rpx;
		
		border: solid #333333;
		
		/* flex布局 */
		display: flex;
		
		/* 布局方向,竖向 */
		flex-direction: column;
		
		/* 竖向居中 */
		justify-content: center;
		/* 横向居中 */
		align-items: center;
	}
	.box-item{
		width: 200rpx;
		height: 200rpx;
		font-size: 30rpx;
		background: #4CD964;
		
		/* 文字项目居中 */
		display: flex;
		justify-content: center;
		align-items: center;
	}
	
	.box-item:nth-of-type(even){
		background: #4CD964;
		/* 不压缩,保持原样 */
		/* flex-shrink: 0; */
		/* 占位置份数 */
		flex: 1
	}
	/* 奇数 */
	.box-item:nth-of-type(odd){
		background: #F0AD4E;
		flex: 3
	}
</style>
