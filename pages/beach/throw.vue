<template>
	<view class="wrapper">
		<view class="input">
			<textarea v-model="info" class="textarea" placeholder="请输入你要发布的内容" />
		</view>
		<view class="footer-button">
			<button type="primary" size="mini" @click="cancel">
				取消
			</button>
			<button type="primary" size="mini" @click="throwAway">
				扔出去
			</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				info: '我爱看超级马力'
			};
		},
		methods: {
			throwAway() {
				uni.navigateBack()
			},
			cancel() {
				uni.navigateBack()
			}
		}
	}
</script>

<style lang="scss">
.wrapper {
	height: calc(100% - 50px);
	padding: 30rpx;
	display: flex;
	flex-direction: column;
	.input {
		flex: 1;
		.textarea {
			height: 95%;
			width: 96%;
			padding: 9px 2%;
			border: 1px solid #E4E7ED
;
		}
	}
	.footer-button {
		margin-top: 30rpx;
		display: flex;
	}
}
</style>
