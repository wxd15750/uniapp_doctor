<template>
	<view class="popupMain">
	    <view class="popupHeader">
	    	<view class="header">
	    		<text class="iconfont icon-xuanxiangqiaguanbianniu"></text>
				<text class="title">请选择服务类型</text>
	    	</view>
			<view class="cards">
				<view class="cardsItem active">
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
		
		<view class="mains">
			<!-- 预约挂号 -->
			<view class="preCode">
				<view class="preHeader">
					<text class="pretitle">预约挂号</text>
					<text class="downline">线下号源</text>
				</view>
				<view class="predesc">
					1.请您在预约时间抵达可是，并在自助机或手机进行预约签到。
				</view>
			</view>
			
			<!-- 挂号时间 -->
			<view class="datanew">
				<view class="dataheader">
					<view class="header_l">
						<text class="iconfont icon-rili"></text>
						<text class="timer">2023年09月</text>
					</view>
					<view class="header_r">
						<text class="iconfont icon-shuaxin"></text>
						<text class="update">更新</text>
					</view>
				</view>
				
				<!-- 时间 -->
				<view class="datas">
					<scroll-view class="scrollview" scroll-x="true" enable-flex="true" >
						<view class="dataItem" v-for="(item,index) in 7" :key="index">
							<text class="wenzi">五</text>
							<text class="nums">15</text>
						</view>
					</scroll-view>
					
				</view>
			</view>
			
			<view class="originCode">
				<view class="originheader">
					<text class="iconfont icon-tianqi"></text>
					<text class="am">上午</text>
					<text class="dataline">剩余号源：50</text>
				</view>
				<view class="origin_duan">
					<view class="timerItem" v-for="(item,index) in 20" :key="index">
						07:50-07:55
					</view>
				</view>
			</view>
			
			<!-- 按钮 -->
			<view class="btn">
				<view class="btnl">
					请选择您要预约的号源
				</view>
				<view class="btns">
					确认按钮
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
	top: 0;
	left: 0;
	width: 100vw;
	box-sizing: border-box;
	background-color: #313b5021;
	
	height: calc(100vh - 164upx);
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
		background-color: #C3E4FF;
		justify-content: space-between;
		z-index:9999;
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
	.mains{
		position: relative;
		padding: 0 20upx;
		top:480upx;
		left: 0;
		height: calc(100vh - 480upx);
		overflow-y: scroll;
		padding-bottom: 100upx;
		.preCode{
			box-sizing: border-box;
			width: 100%;
			height: 196upx;
			background-color: #fff;
			border-radius: 20upx;
			padding: 40upx;
			.preHeader{
				display: flex;
				.pretitle{
					font-size: 28upx;
					color:#000;
					margin-right: 20upx;
					font-weight: 700;
				}
				.downline{
					width: 116upx;
					height: 44upx;
					background-color: #ddf9ee;
					color: #00cf8d;
					text-align: center;
					line-height: 44upx;
					font-size: 24upx;
				}
				
			}
			.predesc{
				font-size: 24upx;
				color:#999999;
				line-height: 36upx;
			}
		}
		.datanew{
			margin-top: 70upx;
			.dataheader{
				display: flex;
				justify-content: space-between;
				align-items: center;
				margin-bottom:32upx;
				.header_l{
					.iconfont{
						width: 32upx;
						height: 32upx;
						color:#0088ff;
						margin-right: 20upx;
					}
					.timer{
						font-size: 26upx;
						color:#000;
					}
				}
				.header_r{
					color:#0088ff;
					.iconfont{
						width: 32upx;
						height: 32upx;
					}
					.update{
						font-size: 24upx;
						margin-left: 10upx;
					}
				}
			}
			
			.datas{
				height: 110upx;
				width: 100%;
				
				.scrollview{
					display: flex;
					width: 100%;
					height: 100%;
					.dataItem{
						flex:1;
						box-sizing: border-box;
						padding: 14upx 0;
						display: flex;
						flex-direction: column;
						justify-content: space-between;
						align-items: center;
						height: 110upx;
						width: 100upx;
						background-color: #f0f8ff;
						border-radius: 10upx;
						margin-right: 20upx;
						.wenzi{
							color:#d5dae3;
							font-size: 24upx;
						}
						.nums{
							font-size: 28upx;
							color:#000;
						}
					}
								
				}
				
			}
			
		}
		.originCode{
			padding-bottom: 200upx;
			.originheader{
				width: 100%;
				margin-top: 40upx;
				margin-bottom: 32upx;
				color:#0088ff;
				font-size: 24upx;
				.am{
					margin:0 30upx 0 20upx
				}
			}
			.origin_duan{
				display: flex;
				justify-content: space-between;
				align-items: center;
				flex-wrap: wrap;
				
				.timerItem{
					width: 220upx;
					height: 80upx;
					margin-bottom: 20upx;
					background-color: #f0f8ff;
					color:#0088ff;
					text-align: center;
					line-height: 80upx;
					font-size: 24upx;
					border-radius: 18upx;
				}
			}
			
			
		}
		
		.btn{
			display: flex;
			position: fixed;
			padding: 0 30upx;
			bottom: 0;
			left: 0;
			width: 100vw;
			height: 140upx;
			justify-content: space-between;
			align-items: center;
			background-color: #fff;
			.btnl{
				font-size: 36upx;
				color:#000;
			}
			.btns{
				width: 220upx;
				height: 80upx;
				text-align: center;
				line-height: 80upx;
				border-radius: 20upx;
				background-color: #0088ff;
				color:#fff;
			}
		}
	}
}
</style>