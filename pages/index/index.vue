<template>
	<view>
		<test :info="20" @fun="fun">
		</test>
		<br/>
		<test2></test2>
		<view>
			子组件向父组件传递的数据为：{{id}}
		</view>
	</view>
</template>

<script>
	import Test from '../../components/Test.vue'
	import Test2 from '../../components/Test2.vue'
	export default {
		components:{
			Test,
			Test2
		},
		
		data() {
			return {
				id:0
			}
		},
		methods: {
          fun(val){
			  this.id=val
		  }
		}
	}
</script>

<style>
	
</style>
