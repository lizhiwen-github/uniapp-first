<template>
	<view>
	   <button @click="getInfo">点我发送get请求</button>
	</view>
</template>

<script>
   export default{
	   methods:{
	   	getInfo (){
	   		uni.request({
	   			url:"http://localhost:8082/api/getlunbo",
	   			success(res) {
	   				console.log(res)
	   			}
	   		})
	   	}		
	   }
   }
</script>

<style>
</style>
