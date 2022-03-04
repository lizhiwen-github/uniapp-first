<template>
	<view>
		<!--
		 view逐渐的使用情况
		 1、hover-calss:view按下去的样式类
		 2、hover-stop-propagation：阻止按下去的冒泡
		 3、hover-start-time：按住多久出现点击状态
		 4、hover-stay-time：手指松开多久，按下状态保持的时间
		 -->
		 <view class="box" hover-class="box-hover">
		<view
		 class="box1" 
		 hover-class="box1-hover"
		 :hover-stop-propagation="true"
		 :hover-start-time="2000"
		 :hover-stay-time="2000"
		 >我是view组件
		 </view>
		 </view>
	</view>
</template>

<script>
</script>

<style>
 .box1{
	 width: 100px;
	 height: 100px;
	 background-color: red;
 }
 .box1-hover{
	 background-color: #007AFF;
 }
 .box{
	 width: 200px;
	 height: 200px;
	 background-color:#4CD964;
 }
 .box-hover{
	 background-color: #3F536E;
 }
</style>
