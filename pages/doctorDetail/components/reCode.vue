<template>
	<view class="recode">
		<view class="remarktag">
			<text class="tagItem active">全部</text>
			<text class="tagItem">仁心仁德（233）</text>
			<text class="tagItem">医术高超（233）</text>
			<text class="tagItem">十分敬业（234）</text>
			<text class="tagItem">回复神速（235）</text>
			<text class="tagItem">妙手回春（233）</text>
			<text class="tagItem">热情亲切（237）</text>
			
		</view>
		
		<view class="remarkList">
			<view class="remarkItem" v-for="(item,index) in 5" :key="index">
				<view class="remarkItem_left">
					<image class="remarkImg" src="../../../static/logo.png" mode=""></image>
				</view>
				<view class="remarkItem_desc">
					
					<view class="remarkItem_desc_l">
						<view class="desc_leftH">
							<view class="desc_texts">
								贺**
							</view>
							<view class="line_btn">
								在线咨询
							</view>
							
						</view>
						<view class="start" >
							<text  class="iconfont icon-xingxing"></text>
							<text  class="iconfont icon-xingxing"></text>
							<text  class="iconfont icon-xingxing"></text>
							<text  class="iconfont icon-xingxing"></text>
							<text  class="iconfont icon-xingxing"></text>
							<text  class="shuzi">5.0</text>
							
						</view>
						<view class="remarkend">
							好评！
						</view>
					</view>
					<view class="remarkItem_desc_data">
						2023-09-05 15:01
					</view>
				</view>
				
			</view>
			
			<view class="more_look">
				查看全部
			</view>
		</view>
	</view> 
	
</template>

<script>
</script>

<style lang="scss">
	.recode{
		width: 100vw;
		padding: 0 20upx;
		background-color: #fff;
		box-sizing: border-box;
		margin-bottom: 132upx;
		.remarktag{
			width: 100%;
			margin: 40upx 0;
			display: flex;
			justify-content: space-between;
			flex-wrap: wrap;
			align-items: center;
			.tagItem{
				width: 230upx;
				height: 52upx;
				background-color:#f4f7fa;
				font-size: 28upx;
				color:#999999;
				text-align: center;
				margin-bottom: 20upx;
				line-height: 52upx;
				border-radius: 10upx;
				&.active{
					background-color: #fff2ea;
					color:#ff8811;
				}
			}
		}
		.remarkList{
			.remarkItem{
				width: 100%;
				height: 124upx;
				display: flex;
				margin-bottom: 52upx;
				// justify-content: space-between;
				.remarkItem_left{
					width: 80upx;
					height: 80upx;
					// border-radius: 50%;
					margin-right: 30upx;
					.remarkImg{
						width: 100%;
						height: 100%;
						border-radius: 50%;
					}
				}
				.remarkItem_desc{
					display: flex;
					flex:1;
					justify-content: space-between;
					.remarkItem_desc_l{
						display: flex;
						flex-direction: column;
						justify-content: space-between;
						.desc_leftH{
							display: flex;
							.desc_texts{
								margin-right: 24upx;
								font-size: 40upx;
								color:#000;
							}
							.line_btn{
								width: 118upx;
								height: 44upx;
								background-color:#d9edff ;
								color:#2e9bff;
								font-size: 28upx;
								line-height:44upx;
							}
						}
						.start{
							width: 28upx;
							height: 28upx;
							color:#ff8811;
							.iconfont{
								font-size: 28upx;
								margin-right: 10upx;
							}
						}
						.remarkend{
							font-size: 28upx;
							color:#a1a1a1;
							    margin-top: 16rpx;
						}
						
					}
					.remarkItem_desc_data{
						font-size: 28upx;
						color:#afafaf;
					}
				}
				
			}
			.more_look{
				text-align: center;
				margin-bottom: 30upx;
				color:#1793ff;
				font-size: 28upx;
			}
		}
	}
</style>