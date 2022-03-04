<template>
	<view id="box">
		<view v-for="(item,index) in list" :key="index">
			{{item}}
		</view>
		<!-- <button @click="freshbtn">点我下拉刷新</button> -->
	</view>
</template>

<script>
export default{
   data(){
	   return{
		   list:['Java','c++','c','php','Python','linux']
	   }
   },
   methods:{
	freshbtn(){
		//自动实现下拉刷新，与自己手动下拉刷新的效果是一样的
		uni.startPullDownRefresh()
	}
   },
   //下拉刷新时，触发的钩子函数
   onPullDownRefresh(){
	   setTimeout(()=>{
		  this.list=['c#','css','html','vue','js']
		  //手动停止下拉刷新，否则不会自动停止刷新
		  uni.stopPullDownRefresh() 
	   },2000)
   },
   // 当滚动条触底时，会触发该事件函数
   onReachBottom(){
	   // ...表示展开数组的意思
	   this.list=[...this.list,...['c#','css','html','vue','js']]
   }
}
</script>

<style>
	#box{
		line-height: 100px;
		height: 1000px;
		
	}
</style>
