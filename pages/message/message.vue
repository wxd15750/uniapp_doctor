<template>
	<view class="container">
		<view class="header">
			<view class="username">
				张三
			</view>
			<view class="arr_right">
				<text class="iconfont icon-a-jiantouyou"></text>
			</view>
		</view>
		<view class="main">
			<view class="tipItem">
				<view class="tip_left">
					<text class="iconfont icon-fenxiang1"></text>
				</view>
				<view class="tip_right">
					<view class="tipHeader">
						待办提醒
					</view>
					<view class="content">
						暂无最新通知
					</view>
				</view>
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
	padding: 0 30upx;
	box-sizing: border-box;
	.header{
		display: flex;
		box-sizing: border-box;
		justify-content: space-between;
		padding: 0 20upx;
		align-items: center;
		width: 100%;
		height: 84upx;
		background-color: #e0f0ff;
		border-radius: 10upx;
		.arr_right{
			width: 30upx;
			height: 30upx;
			color:#226fff;
			font-weight: 700;
			font-size:28upx;
			
		}
		
	}
	.main{
		width: 100%;
		margin-top: 20upx;
		.tipItem{
			display: flex;
			justify-content: space-between;
			align-items: center;
			.tip_left{
				width: 100upx;
				height: 100upx;
				background-color: #ffd529;
				margin-right: 20upx;
				border-radius: 50%;
				line-height: 100upx;
				text-align: center;
				color:#fff;
				.iconfont{
					font-size:64upx;
				}
			}
			.tip_right{
				display: flex;
				flex: 1;
				height: 100upx;
				flex-direction: column;
				justify-content: space-between;
				.tipHeader{
					font-size: 32upx;
				}
				.content{
					font-size: 24upx;
					color: #8f9399;
				}
			}
			
		}
	}
}
</style>
