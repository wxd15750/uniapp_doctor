<template>
	<view class="container">
		<view class="bannerImg">
			<image src="../../static/logo.png" mode=""></image>
			<text>收藏按钮</text>
		</view>
		<view class="btn">
			<view class="context">
				预约服务
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
.container{
	width: 100vw;
	height: 100vh;
	box-sizing: border-box;
	.bannerImg{
		
	}
	.btn{
		position: fixed;
		left: 0;
		bottom: 0;
		width: 100%;
		padding: 20upx;
		box-sizing: border-box;
		.context{
			background-color: #414dff;
			color:#fff;
			font-size: 32upx;
			height: 80upx;
			display: flex;
			justify-content: center;
			align-items: center;
			border-radius: 10upx;
		}
	}
}
</style>
