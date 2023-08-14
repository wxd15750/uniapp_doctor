<template>
	<view class="container">
		<view class="header">
			<view class="card">
				<view class="userAvator">
					<image class="avator" src="../../static/logo.png" mode=""></image>
				</view>
				<view class="userInfo">
					<view class="headers">
						<view class="usernames">
							张三
						</view>
						<view class="renzheng">
							已认证
						</view>
					</view>
					<view class="sessions">
						<view class="mannger">
							就诊人管理
						</view>
						<view class="arr-right">
							<text class="iconfont icon-a-jiantouyou"></text>
						</view>
						
					</view>
				</view>
				
			</view>
		</view>
		
		<view class="main">
			<view class="navCard">
				<view class="navCard">
					挂号记录
				</view>
				<view class="navCard">
					咨询记录
				</view>
			</view>
			
			<view class="serve">
				<view class="serve_header">
					我的服务
				</view>
				<view class="serve_bd">
					<view class="serve_bdItem">
						<view class="iconImg">
							<text class="iconfont icon-shoucang"></text>
						</view>
						<view class="title">
							我的收藏
						</view>
					</view>
					<view class="serve_bdItem">
						<view class="iconImg">
							<text class="iconfont icon-jiaoyifenxi"></text>
						</view>
						<view class="title">
							交易记录
						</view>
					</view>
					<view class="serve_bdItem">
						<view class="iconImg">
							<text class="iconfont icon-kefu"></text>
						</view>
						<view class="title">
							我的客服
						</view>
					</view>
					<view class="serve_bdItem">
						<view class="iconImg">
							<text class="iconfont icon-suifangguanli"></text>
						</view>
						<view class="title">
							我的随访
						</view>
					</view>
					<view class="serve_bdItem">
						<view class="iconImg">
							<text class="iconfont icon-shezhi"></text>
						</view>
						<view class="title">
							设置
						</view>
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
	width: 100%;
	height: 100%;
	box-sizing: border-box;
	.header{
		display: flex;
		justify-content: center;
		align-items: flex-end;
		width: 100%;
		height: 400upx;
		background-color: #00ffff;
		padding: 0 30upx;
		box-sizing: border-box;
		.card{
			display: flex;
			justify-content: space-between;
			box-sizing: border-box;
			padding:40upx 30upx;
			width: 100%;
			height: 200upx;
			background-color: #ffff00;
			border-radius: 20upx;
			.userAvator{
				display: flex;
				justify-content: space-between;
				width: 100upx;
				height: 100upx;
				border-radius: 50%;
				border: 4upx solid #fff;
				margin-right: 20upx;
				.avator{
					width: 100%;
					height: 100%;
					border-radius: 50%;
				}
				
			}
			.userInfo{
				display: flex;
				flex-direction: column;
				justify-content: space-between;
				flex:1;
					.headers{
						display: flex;
						.usernames{
							font-weight: 700;
							color:#fff;
							font-size: 36upx;
							margin-right:10upx;
						}
						.renzheng{
							width: 80upx;
							font-size: 20upx;
							height: 30upx;
							color:#ff8630;
							background-color: #ffed82;
							border-radius: 10upx;
							line-height: 30upx;
							text-align: center;
						}
					}
					.sessions{
						display: flex;
						justify-content: space-around;
						font-size:24upx;
						align-items: center;
						width: 170upx;
						height: 50upx;
						text-align:center;
						background-color: rgba(0, 0, 0, .4);
						border-radius: 30upx;
						padding:0 10upx;
						.mannger{
							color:#fff;
						}
						.arr-right{
							width: 26upx;
							height: 26upx;
							background: #fff;
							font-size:24upx;
							border-radius: 50%;
							line-height: 26upx;
							.iconfont{
								font-size:24upx;
							}
						}
					}
				}
		}
	}
	.main{
		padding: 0 30upx;
		background-color: #ccc;
		height: calc(100vh - 400upx);
		.navCard{
			margin: 20upx 0;
			display: flex;
			justify-content: space-between;
			.navCard{
				display: flex;
				justify-content: center;
				align-items: center;
				width: 330upx;
				height: 154upx;
				background-color: #afd6ff;
				border-radius: 20upx;
				font-weight: 700;
				font-size: 32upx;
				color:#377e9f;
			}
		}
		.serve{
			box-sizing: border-box;
			padding:30upx 20upx 40upx;
			background-color: #fff;
			width: 100%;
			// height: 200upx;
			border-radius: 20upx;
			.serve_header{
				font-size: 32upx;
				font-weight: 700;
				color:#000;
			}
			.serve_bd{
				width: 100%;
				display: flex;
				flex-wrap: wrap;
				justify-content: space-between;
				.serve_bdItem{
					display: flex;
					margin-top: 40upx;
					flex-direction: column;
					justify-content: space-between;
					align-items: center;
					width: 140upx;
					height: 108upx;
					// background-color: #55ff7f;
					.iconImg{
						width: 54upx;
						height: 54upx;
						// background-color: #ffff00;
						.iconfont{
							font-size:54upx;
						}
					}
					.title{
						font-size: 24upx;
						color:#000;
						text-align: center;
					}
				}
			}
		}
	}
}
</style>
