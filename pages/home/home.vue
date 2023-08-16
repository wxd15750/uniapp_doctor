<template>
	<view class="content">
		<view class="header">
			<view class="logo">
				<image class="Img" src="../../static/logo.png" mode=""></image>
			</view>
			<view class="searchInp" @click="toSearch">
				<text  class="iconfont icon icon-fenxiang"></text>
				<text class="shopTip">输入关键字搜索医师</text>
			</view>
		</view>
		
		<view class="main">
			<view class="navList">
				<view class="navItem">
					<text class="navtitle">预约挂号</text>
				</view>
				<view class="navItem">
					<text class="navtitle">门诊缴费</text>
				</view>
				<view class="navItem">
					<text class="navtitle">在线咨询</text>
				</view>
				<view class="navItem">
					<text class="navtitle">网络门诊</text>
				</view>
				
			</view>
			
			<view class="userInfo">
				<view class="infoLeft">
					<view class="leftup">
						<view class="info">
							<text class="names">张三</text>
							<view class="btn">
								切换
							</view>
						</view>
						<view class="telCode">
							门诊号【<text class="tel">55031235648</text>】
						</view>
					</view>
					<view class="leftdown">
						暂无待办事项
					</view>
				</view>
				<view class="infoRight">
					<image class="erweima" src="../../static/logo.png" mode=""></image>
				</view>
			</view>
			
			<view class="serve">
				<view class="serve_header">
					<text class="serveItem ">门诊服务</text>
					<text class="serveItem active">住院服务</text>
					<text class="serveItem">便捷服务</text>
				</view>
				
				<view class="serve_body">
					<view class="serve_body_item">
						<image class="Img" src="../../static/logo.png" mode=""></image>
						<text class="title">建卡/绑卡</text>
					</view>
					<view class="serve_body_item">
						<image class="Img" src="../../static/logo.png" mode=""></image>
						<text class="title">报告查询</text>
					</view>
					<view class="serve_body_item">
						<image class="Img" src="../../static/logo.png" mode=""></image>
						<text class="title">送药到家</text>
					</view>
					<view class="serve_body_item">
						<image class="Img" src="../../static/logo.png" mode=""></image>
						<text class="title">配送订单</text>
					</view>
					
				</view>
				
				<view class="serve_footer">
					<text class="line"></text>
				</view>
			</view>
			<view class="banner">
				<u-swiper
				    :list="list1"
				    height="140"
					radius="10"
					indicator="true"
					indicatorMode="dot"
					indicatorStyle="dot"
				></u-swiper>
			</view>
			<view class="mydoctor">
				<view class="doctor_header">
					我的
					<text class="light">医生</text>
				</view>
				
				<DcoctorList></DcoctorList>
					
					<!-- <view class="doctorItem">
						<view class="doctorImg">
							<image class="doctor_avator" src="../../static/logo.png" mode=""></image>
						</view>
						<view class="doctorInfo">
							<view class="doctor_name">
								<text class="names">张碧晨</text>
								<text class="remark">5.0</text>
							</view>
							<view class="skill">
								<text class="job_name">副主任医师</text>
								<text class="productment">外科</text>
							</view>
							
						</view>
						<view class="mark">
							有号
						</view>
					</view> -->
					
					
				
			</view>
			
			
		</view>
		
	</view>
</template>

<script>
	import DcoctorList from '../../components/docotrList/docotrList.vue'
	export default {
		data() {
			return {
				 list1: [
				    'https://cdn.uviewui.com/uview/swiper/swiper1.png',
				    'https://cdn.uviewui.com/uview/swiper/swiper2.png',
				    'https://cdn.uviewui.com/uview/swiper/swiper3.png',
				]
			}
		},
		onLoad() {

		},
		components:{
			DcoctorList
		},
		methods: {
			toSearch(){
				uni.navigateTo({
					url:"/pages/search/search"
				})
			}
		}
	}
</script>

<style lang="scss">
.content {
	width: 100vw;
	height: 100%;
	.header {
		box-sizing: border-box;
		position: fixed;
		top: 0;
		left: 0;
		width: 100vw;
		padding: 0 30upx 30upx;
		background-color: #bcdfdf;
		z-index:999999;
		
		.logo{
			padding-top: 20upx;
			height: 100upx;
			.Img{
				width: 300upx;
				height: 100%;
			}
		}
		.searchInp{
			display: flex;
			align-items: center;
			width: 100%;
			height: 80upx;
			font-size: 28upx;
			padding-left: 40upx;
			box-sizing: border-box;
			border-radius: 28upx;
			background-color: #fff;
			color:#4a4a4a;
			.icon{
				font-size: 40upx;
				margin-right: 20upx;
				color:#ababab;
			}

		}
	}
	
	.main{
		height: calc(100vh - 230upx);
		margin-top: 230upx;
		padding: 0 30upx;
		.navList{
			display: flex;
			justify-content: space-between;
			width: 100%;
			.navItem{
				display: flex;
				width: 160upx;
				height: 160upx;
				border-radius: 30upx;
				background-color: #4a4a4a;
				justify-content: center;
				.navtitle{
					font-size: 30upx;
					margin-top: 20upx;
					// text-align: center;
					color:#fff;
					
				}
			}
		}
		
		.userInfo{
			margin-top: 20upx;
			padding: 30upx;
			display: flex;
			justify-content: space-between;
			align-items: center;
			background-color: #c5cdff;
			border-radius: 20upx;
			.infoLeft{
				.leftup{
					.info{
						display: flex;
						align-items: center;
						margin-bottom: 16upx;
						.names{
							font-weight: 700;
							font-size: 38upx;
							color:#282828;
							margin-right: 20upx;
						}
						.btn{
							width: 80upx;
							height: 38upx;
							font-size:24upx;
							text-align: center;
							color:#fff;
							border-radius: 0upx 20upx 0upx 20upx;
							background-color: #1573ff;
						}
					}
					.telCode{
						font-size: 28upx;
						color:#909090;
						.tel{
							font-size: 24upx;
						}
					}
				}
				.leftdown{
					color: #00aaff;
					margin-top: 16upx;
					font-size: 24upx;
				}
				
			}
			.infoRight{
				width: 100upx;
				height: 100upx;
				.erweima{
					width: 100%;
					height: 100%;
					
				}
			}
		}
		
		.serve{
			margin-top: 20upx;
			border:2upx solid #c1d1d1;
			border-radius: 20upx;
			padding:0 20upx;
			.serve_header{
				display: flex;
				justify-content: space-between;
				align-items: center;
				width: 100%;
				height: 80upx;
				.serveItem{
					flex:1;
					text-align: center;
					height: 100%;
					line-height: 80upx;
					border-radius: 0 0 20upx 20upx;
					
				}
				.active{
					background-color: #00aaff;
					color:#fff;
				}
				
			}
			
			.serve_body{
				display: flex;
				justify-content: space-around;
				align-items: center;
				flex-wrap: wrap;
				width: 100%;
				height: 300upx;
				.serve_body_item{
					display: flex;
					flex-direction: column;
					justify-content: space-between;
					align-items: center;
					width: 25%;
					text-align: center;
					color: #868686;
					height: 100upx;
					.Img{
						width: 50upx;
						height: 50upx;
					}
					.title{
						font-size: 28upx;
					}
					
				}
				&::after{
					content:'';
					display: block;
					width: 100%;
					height: 100upx;
				}
				
				
				
			}
			.serve_footer{
				display: flex;
				justify-content: center;
				padding-bottom: 30upx;
				.line{
					width: 30upx;
					height: 10upx;
					border-radius: 10upx;
					background-color: #00aaff;
				}
			}
		}
		
		.banner{
			margin-top: 20upx;
			width: 100%;
			// height: 200upx;
			background-color: #00aaff;
			border-radius: 20upx;
			
		}
		
		.mydoctor{
			width: 100%;
			height: 100upx;
			margin-top: 20upx;
			.doctor_header{
				width: 132upx;
				height: 60upx;
				line-height: 60upx;
				border-radius: 30upx;
				background-image:linear-gradient(to right, #f8f7ff 10%, #d2e0ff);
				color:#747474;
				font-size:28upx;
				.light{
					color:#319cff;
				}
			}
			// .doctor_bd{
			// 	// margin-top: 20upx;
			// 	// display: flex;
			// 	// justify-content: space-between;
			// 	// flex-wrap: wrap;
			// 	// .doctorList{
			// 	// 	width: 274upx;
			// 	// }
			// }
			
		}
		
	}
}

	
</style>
