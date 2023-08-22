<template>
	<view class="container">
		<view class="bannerImg">
			<image class="Img" src="../../static/logo.png" mode=""></image>
			<text class="shoubtn">收藏按钮</text>
		</view>
		
		<view class="doctorIntro">
			<view class="doctorInfo">
				<view class="username">
					张碧晨
				</view>
				<view class="productment">
					主任医师
					<text class="pinfen">5.0</text>
				</view>
			</view>
		</view>
		
		<view class="hospitalCard">
			<view class="headers">
				<text class="types">三甲</text>
				<text class="hospitalName">程序员疯人院—消化内科</text>
			</view>
			
			<view class="doctorPro">
				<text class="doctors">医师简介</text>
				<text class="doctorSkill">息肉切除，取异物，EMR手术，食管静脉套扎术，食管静脉硬化剂注射术，胃...
					<text class="textDetail">详情</text>
				</text>
			</view>
			<view class="skills">
				<view class="skillItems">
					EMR手术
				</view>
				<view class="skillItems">
					食管静脉套扎术
				</view>
				<view class="skillItems">
					胃底静脉组织胶注射术
				</view>
			</view>
			
			<view class="datasList">
				<view class="dataItems">
					<view class="numbers">
						129
					</view>
					<view class="descrt">
						患者咨询/次
					</view>
				</view>
				<view class="dataItems">
					<view class="numbers">
						0
					</view>
					<view class="descrt">
						线上接诊/例
					</view>
				</view>
				<view class="dataItems">
					<view class="numbers">
						1245
					</view>
					<view class="descrt">
						线下接诊/例
					</view>
				</view>
			</view>
		</view>
		
		<view class="tabs">
			<u-tabs :list="list1"></u-tabs>
			
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
				list1: [
					{
				        name: '关注',
				    },
					{
				        name: '推荐',
				    }, 
					{
				        name: '电影'
				    },
				]
			};
		}
	}
</script>

<style lang="scss">
.container{
	width: 100vw;
	height: 100vh;
	box-sizing: border-box;
	background-color: #ccc;
	.bannerImg{
		position: relative;
		top: 0;
		left: 0;
		width: 100vw;
		height: 300upx;
		.Img{
			position: absolute;
			top: 0;
			left: 0;
			width: 100%;
			height: 100%;
		}
		.shoubtn{
			position: absolute;
			top: 20upx;
			right: 24upx;
			width: 40upx;
			height: 40upx;
			border-radius: 50%;
			background-color: rgba(0, 0, 0, .2);
		}
		
		
	}
	
	.doctorIntro{
		position: relative;
		top: 0;
		left: 0;
		width: 100vw;
		height: 90upx;
		background-color: #bcd6ff;
		.doctorInfo{
			position: absolute;
			bottom: 0;
			left: 0;
			padding: 20upx 30upx 20upx 30upx;
			box-sizing: border-box;
			width: 300upx;
			background-color: #a1e2ff;
			.username{
				font-size: 32upx;
				
			}
			.productment{
				font-size: 28upx;
				margin-top: 10upx;
				.pinfen{
					padding: 0 10upx;
					height: 30upx;
					line-height: 30upx;
					color:#ff7423;
					margin-left: 4upx;
				}
			}
		}
	}
	
	.hospitalCard{
		width: 100%;
		padding: 20upx 20upx 40upx;
		box-sizing: border-box;
		background-color: #fff;
		.headers{
			display: flex;
			align-items: center;
			.types{
				width: 50upx;
				text-align:center;
				height: 30upx;
				background-color: #ffd08e;
				color: #ff8c08;
				font-size: 20upx;
				margin-right: 10upx;
			}
			.hospitalName{
				font-weight: 700;
				font-size: 28upx;
				color:#000;
			}
		}
		.doctorPro{
			margin-top: 20upx;
			width: 100%;
			// height: 80upx;
			.doctors{
				padding: 10upx 5upx;
				font-size: 20upx;
				color:#3f70cc;
				background-color: rgba(119, 167, 208, 0.2);
				margin-right: 10upx;
			}
			.doctorSkill{
				box-sizing: border-box;
				font-size: 28upx;
				color:#a4b3ab;
				.textDetail{
					color:#3f70cc;
					border-bottom:2upx solid #3f70cc;
					
				}
				
			}
		}
		
		.skills{
			margin-top: 15upx;
			display: flex;
			justify-content: space-between;
			.skillItems{
				height: 40upx;
				line-height: 40upx;
				font-size:24upx;
				color: #414dff;
				padding: 0 20upx;
				background-color: #84a9cc;
				border-radius: 10upx;
				
			}
		}
		
		.datasList{
			margin-top: 20upx;
			display: flex;
			justify-content: space-around;
			align-items: center;
			width: 100%;
			background-color: #fff3af;
			border-radius: 10upx;
			box-sizing: border-box;
			padding: 30upx 40upx;
			.dataItems{
				color:#614903;
				height: 100%;
				font-weight: 700;
				text-align: center;
				.numbers{
					font-size: 28upx;
				}
				.descrt{
					font-size: 24upx;
				}
			}
		}
	}
	
	.tabs{
		margin-top: 20upx;
		width: 100vw;
		background-color: #fff;
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
