<template>
	<view class="wrapper">
		<view class="header">
			<view class="avatar">
				<image src="../../static/img/qa.png" mode="aspectFit"></image>
			</view>
			<view class="sex">
				{{personInfo.sex}}
			</view>
			<view class="sign">
				{{personInfo.sign}}
			</view>
		</view>
		<view class="information">

		</view>
		<view class="footer-button">
			<button type="primary" size="mini" @click="throwAway">
				扔掉
			</button>
			<button type="primary" size="mini" @click="reply">
				回复
			</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				personInfo: {
					sex: '男',
					sign: '开朗幽默的掘金着'
				}
			};
		},
		methods: {
			throwAway() {
				uni.navigateBack()
			},
			reply(){}
		}
	}
</script>

<style lang="scss">
	.wrapper {
		height: calc(100% - 50px);
		padding: 30rpx;
		display: flex;
		flex-direction: column;
		.header {
			display: flex;
			align-items: center;
		
			.avatar {
				width: 100rpx;
				height: 100rpx;
				margin-right: 20rpx;
		
				image {
					height: 100%;
					width: 100%;
				}
			}
			.sex {
				margin-right: 20rpx;
			}
		}
		.information {
			flex: 1;
		}
		.footer-button {
			display: flex;
			margin: 30rpx;
		}
	}
</style>
