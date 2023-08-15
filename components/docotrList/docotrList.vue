<template>
	<view class="doctor_bd">
		<view class="doctorItem">
			<view class="doctorImg">
				<image class="doctor_avator" src="../../static/logo.png" mode=""></image>
			</view>
			<view class="doctorInfo">
				<view class="doctor_name">
					<text class="names">林涛</text>
					<text class="remark">5.0</text>
				</view>
				<view class="skill">
					<text class="job_name">副主任医师</text>
					<text class="productment">皮肤整形科</text>
				</view>
			</view>
			<view class="mark">有号</view>
		</view>
		<view class="doctorItem">
			<view class="doctorImg">
				<image class="doctor_avator" src="../../static/logo.png" mode=""></image>
			</view>
			<view class="doctorInfo">
				<view class="doctor_name">
					<text class="names">张碧晨</text>
					<text class="remark">5.0</text>
				</view>
				<view class="skill">
					<text class="job_name">主任医师</text>
					<text class="productment">心脏科</text>
				</view>
			</view>
			<view class="mark">有号</view>
		</view>
		<view class="doctorItem">
			<view class="doctorImg">
				<image class="doctor_avator" src="../../static/logo.png" mode=""></image>
			</view>
			<view class="doctorInfo">
				<view class="doctor_name">
					<text class="names">刘亦菲</text>
					<text class="remark">5.0</text>
				</view>
				<view class="skill">
					<text class="job_name">副主任医师</text>
					<text class="productment">心理科</text>
				</view>
			</view>
			<view class="mark">有号</view>
		</view>
	</view>
</template>

<script>
export default {
	name: 'DocotrList',
	data() {
		return {};
	}
};
</script>

<style lang="scss">
.doctor_bd{
	width: 100%;
	margin-top: 20upx;
	display: flex;
	justify-content: space-between;
	flex-wrap: wrap;
	.doctorItem{
		position: relative;
		width: 48%;
		height: 300upx;
		border-radius: 20upx;
		margin-bottom:20upx;
		.doctorImg{
			width: 100%;
			height: 100%;
			border-radius: 20upx;
			.doctor_avator{
			width: 100%;
			height: 100%;
			}
		}
		.doctorInfo{
			position: absolute;
			width: 274upx;
			left: 0;
			bottom:0;
			border-radius: 20upx 20upx 0 0;
			padding: 20upx 30upx;
			background-image:linear-gradient(to right, #b9e9ff, #e5f8ff);
			.doctor_name{
				display: flex;
				align-items: center;
				width: 370upx;
				box-sizing: border-box;

				.names{
					font-size:32upx;
					margin-right: 10upx;
					
				}
				.remark{
					width: 60upx;
					text-align: center;
					height: 26upx;
					line-height: 26upx;
					background-color: #ffe895;
					border-radius: 13upx;
					font-size:26upx;
					color:#ffb32e;
				}
			}
			.skill{
				font-size: 26upx;
				color:#7c7c7c;
			}
		}
		.mark{
			position: absolute;
			top: 0;
			right: 0;
			width: 80upx;
			height: 36upx;
			font-size:28upx;
			border-radius: 18upx 18upx 0 18upx;
			background-color: #3041de;
			color:#fff;
			text-align: center;
			line-height:36upx;
			
		}
	}
}
</style>
