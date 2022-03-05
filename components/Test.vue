<template>
	<view>
		父组件传递给Test组件的值为：{{info}}
		从Test2组件中获取的数据为：{{val}}
		<button>点击修改</button>
	</view>
</template>

<script>
	export default {
		created() {
		   uni.$on('fun1',res=>{
			   console.log(res)
			   this.val=res
		   })	
		},
		props:{
			info:{
				type:Number,
				default:0,
				required:true
			}
		},
		name:"Test",
		data() {
			return {
				id:20,
				val:0
			};
		},
		mounted() {
			this.$emit("fun",this.id)
		}
	}
</script>

<style>

</style>
