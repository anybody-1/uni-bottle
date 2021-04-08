<template>
	<view class="wrapper">
		<view class="header">
			<view class="avatar">
				<image src="../../static/img/qa.png" mode="aspectFit"></image>
			</view>
			<view class="userInfo">
				<view class="name">
					<text>{{userInfo.userName}}</text>/
					<text>{{userInfo.sex}}</text>
					<uni-icons type="star" color="blue" class="vip-type"></uni-icons>
				</view>
				<view class="follow">
					<text class="item">粉丝<text class="number">{{userInfo.fans}}</text></text>
					<text>关注<text class="number">{{userInfo.follow}}</text></text>
				</view>
			</view>
		</view>
		<view class="content">
			<view class="options">
				<uni-list>
				    <!-- <uni-list-item title="开启点击反馈" clickable  @click="onClick" ></uni-list-item> -->
				    <uni-list-item title="开通/加持VIP" link to="/pages/vue/index/index" @click="onClick($event,1)" ></uni-list-item>
				    <uni-list-item title="我的心情" link="reLaunch" to="/pages/vue/index/index" @click="onClick($event,1)" ></uni-list-item>
				    <uni-list-item title="关注的心情" link="reLaunch" to="/pages/vue/index/index" @click="onClick($event,1)" ></uni-list-item>
				    <uni-list-item title="用户黑名单" link="reLaunch" to="/pages/vue/index/index" @click="onClick($event,1)" ></uni-list-item>
				</uni-list>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				userInfo: {
					userName: '永',
					sex: '男',
					vip: 1,
					fans: 10,
					follow: 5
				}
			};
		}
	}
</script>

<style lang="scss" scoped>
.wrapper {
	height: 100%;
	display: flex;
	flex-direction: column;
} 
.header {
	display: flex;
	padding: 20rpx;
	.avatar {
		width: 100rpx;
		height: 100rpx;
		margin-right: 20rpx;
		image {
			height: 100%;
			width: 100%;
		}
	}
	.userInfo {
		flex: 1;
		.name {
			margin-bottom: 10rpx;
		}
		.vip-type {
			margin-left: 20rpx;
		}
		.follow {
			.item {
				margin-right: 30rpx;
			}
			.number {
				margin-left: 10rpx;
			}
		}
	}
}
.content {
	background-color: #E5E5E5;
	flex: 1;
	.options {
		margin-top: 20rpx;
	}
}
</style>
