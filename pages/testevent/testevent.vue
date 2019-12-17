<template>
	<view>
		<text>{{name}}</text>
		<view class="box1" @tap="click1()">
			外边
			<view class="box2" @tap.stop="click2()">里边</view>			
		</view>	
	</view>
</template>

<script>
	export default {
		data() {
			return {
				name : "哈哈哈"
			}
		},
		methods: {
			
			click1:function(){
				console.log("点击了外部")
				this.name = "呵呵呵呵"
			},
			click2 : function(){
				console.log("点击了里边")
			}
		}
	}
</script>

<style>
	.box1{
		width: 100%;
		height: 200rpx;
		background: #007AFF;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.box2{
		width: 100rpx;
		height: 100rpx;
		background: #4CD964;
	}

</style>
