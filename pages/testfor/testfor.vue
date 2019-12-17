<template>
	<view>
		<!-- 要使用key进行绑定索引，否则会报错 -->
		<view v-for="(val,index) in data1" :key="index">
			{{index}} - {{val}}
		</view>
		<text>-------------------------------------</text>
		<view v-for="(val,index) in data2" :key="index">
			{{index}} - {{val}}
		</view>
		<text>-------------------------------------</text>
		<!-- 双层循环 -->
		<view v-for="(val1,index1) in data3" :key="index1">
			<view v-for="(val2,index2) in val1.values" :key="index2">
				{{val2}}
			</view>
			<text>===</text>
		</view>
		<text>-------------------------------------</text>
		<!-- 推荐使用block做逻辑 -->
		<block v-for="(val,index) in data1" :key="index">
			<view>{{val}}</view>
		</block>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				data1:["a","b","c"],
				data2:{
					"name":"hhh",
					"age":2
				},
				data3:[
					{
						"name":"a",
						"values":[1,2,3]
					},
					{
						"name":"b",
						"values":[4,5,6]
					}
				]
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
