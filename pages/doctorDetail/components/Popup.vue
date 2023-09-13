<template>
	<view class="popupMain">
	    <view class="popupHeader">
	    	<view class="header">
	    		<text class="iconfont icon-xuanxiangqiaguanbianniu"></text>
				<text class="title">请选择服务类型</text>
	    	</view>
			<view class="cards">
				<view class="cardsItem">
					<view class="Imgicon">
						<image class="imgs" src="../../../static/logo.png" mode=""></image>
					</view>
					<text class="desc">线下号源</text>
				</view>
				<view class="cardsItem">
					<view class="Imgicon">
						<image class="imgs" src="../../../static/logo.png" mode=""></image>
					</view>
					<text class="desc">网络门诊</text>
				</view>
				<view class="cardsItem">
					<view class="Imgicon">
						<image class="imgs" src="../../../static/logo.png" mode=""></image>
					</view>
					<text class="desc">在线咨询</text>
				</view>
			</view>
	    </view>
	</view>
</template>

<script>
</script>

<style lang="scss" scoped>
.popupMain{
	position: relative;
	width: 100vw;
	padding: 0 20upx;
	background-color: #fff;
	border-radius: 20upx 20upx 0 0;
	.popupHeader{
		position: fixed;
		top: 164upx;
		left: 0;
		width: 100vw;
		box-sizing: border-box;
		border-radius: 20upx 20upx 0 0;
		padding: 60upx 20upx;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		background-color: #C3E4FF;
		.header{
			display: flex;
			margin-bottom: 60upx;
			.iconfont{
				width: 36upx;
				height: 36upx;
				font-size: 36upx;
				color:#8f9399;
			}
			.title{
				flex: 1;
				text-align: center;
				font-weight: 700;
				font-size:40upx ;
				color:#000;
			}
		}
		.cards{
			display: flex;
			justify-content: space-between;
			.cardsItem{
				width: 220upx;
				height: 240upx;
				background-color: #fff;
				border-radius: 20upx;
				display: flex;
				justify-content: center;
				align-items: center;
				flex-direction: column;
				overflow: hidden;
				.Imgicon{
					width: 104upx;
					height: 104upx;
					.imgs{
						width: 100%;
						height: 100%;
					}
				}
				.desc{
					font-size: 28upx;
					margin-bottom: 30upx;
				}
				&.active{
					border: 2upx solid #0188ff;
				}
			}
		}
	}
}
</style>