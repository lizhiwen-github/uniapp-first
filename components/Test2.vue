<template>
	<view>
		<button @click="fun">点击按钮向Test组件传值</button>
	</view>
</template>

<script>
	export default {
		name:"Test2",
		data() {
			return {
				id:88
			};
		},
		methods:{
			fun(){
				uni.$emit("fun1",this.id)
			}
		}
	}
</script>

<style>

</style>
