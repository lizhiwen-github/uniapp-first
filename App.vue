<script>
	export default {
		// 应用的生命周期函数
		// onLanuch:当项目初始化完成时触发
		// onShow:当项目显示时被触发
		// onHide：当项目隐藏时被触发
		// onError:当项目报错时被触发
		onLaunch: function() {
			console.log('项目初始化完成')
		},
		onShow: function() {
			console.log('项目显示')
		},
		onHide: function() {
			console.log('项目隐藏')
		},
		onError(err) {
			console.log(err)
		}
	}
</script>

<style>
	/*每个页面公共css */
	@import url("./static/fonts/iconfont.css");
</style>
