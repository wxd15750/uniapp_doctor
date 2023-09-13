<template>
	<view class="container">
		<view class="header">
			<view class="arr_r" @click="goback">
				<text class="iconfont icon-arrow-left-01-sharp"></text>
			</view>
			<view class="search">
				<input class="Inp" type="text" value="" placeholder="输入关键字搜索医师" />
				<text  class="iconfont searchBtn icon-fenxiang"></text>
				
			</view>
		</view>
		
		<view class="main">
			<view class="hot">
				<view class="hottitle">
					热门搜索
				</view>
				<view class="hotmain">
					<view class="hot_item">
						体检科
					</view>
					<view class="hot_item">
						中医科
					</view>
					<view class="hot_item">
						妇科
					</view>
					<view class="hot_item">
						消化内科
					</view>
					<view class="hot_item">
						神经内科
					</view>
					<view class="hot_item">
						肛肠科
					</view>
					
				</view>
			</view>
			
			<view class="recomm">
				<view class="recom_title">
					<view class="line_left">
						
					</view>
					<view class="desc">
						为您推荐专家名医
					</view>
					<view class="line_right">
						
					</view>
				</view>
				
				<DcoctorList></DcoctorList>
			</view>
		</view>
		
		
	</view>
</template>

<script>
	import DcoctorList from '../../components/docotrList/docotrList.vue'
	export default {
		data() {
			return {
				
			};
		},
		components:{
			DcoctorList
		},
		methods:{
			goback(){
				uni.switchTab({
					url:"/pages/home/home"
				})
			}
		}
	}
</script>

<style lang="scss">
.container{
	width: 100%;
	// background-color: #ccc;
	.header{
		display: flex;
		align-items: center;
		position: fixed;
		top:30upx;
		left: 0;
		height: 100upx;
		box-sizing: border-box;
		z-index: 99999;
		background-color: #fff;
		.arr_r{
			margin: 0 20upx;
			height: 50upx;
			
			.iconfont{
				font-size: 40upx;
				font-weight: 700;
				line-height: 50upx;
			}
		}
		.search{
			position: relative;
			width: 350upx;
			height: 50upx;
			.Inp{
				width: 100%	;
				height: 50upx;
				background-color: #e9ebef;
				font-size:24upx;
				border-radius: 10upx;
				padding: 0 10upx;
				line-height: 50upx;
			}
			.searchBtn{
				position: absolute;
				top:10upx;
				right: 0;
			}
			
		}
	}
	
	.main{
		padding: 0 30upx;
		margin-top: 130upx;
		box-sizing: border-box;
		height: calc(100vh - 100upx);
		width: 100vw;
		.hot{
			width: 100%;
			.hottitle{
				font-size: 24upx;
				color:#000;
			}
			.hotmain{
				display: flex;
				flex-wrap: wrap;
				width: 100%;
				margin-top: 20upx;
				.hot_item{
					box-sizing: border-box;
					padding: 0 20upx;
					height: 40upx;
					margin-bottom: 20upx;
					margin-right: 10upx;
					line-height: 40upx;
					text-align: center;
					border-radius: 10upx;
					background-color: #faf1ea;
					font-size: 24upx;
					color:#ff8811;
				}
			}
		}
		
		.recomm{
			margin-top: 40upx;
			margin-bottom: 20upx;
			.recom_title{
				display: flex;
				align-items: center;
				width: 100%;
				height: 40upx;
				// background-color: #cc7122;
				.line_left{
					height: 2upx;
					width: 230upx;
					background-image: linear-gradient(to right, #fff,#bfbfbf);
				}
				.line_right{
					height: 2upx;
					width: 230upx;
					background-image: linear-gradient(to right, #bfbfbf,#fff);
				}
				.desc{
					font-size:24upx;
					color:#bec2cc;
					padding: 0 24upx;
				}
			}
		}
	}
}
</style>
