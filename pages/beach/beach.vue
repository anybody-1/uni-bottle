<template>
	<view class="content">
		<view class="image">
			<image src="../../static/img/beach.png" mode="aspectFill"></image>
		</view>
		<view class="footer-button">
			<button type="primary" size="mini" @click="goto('/pages/beach/fishing')">
				捞一捞
			</button>
			<button type="primary" size="mini" @click="goto('/pages/beach/throw')">
				扔一个
			</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			};
		},
		onLoad() {},
		methods: {
			goto(url) {
				uni.navigateTo({
					url: url
				})
			}
		}
	};
</script>

<style lang="scss" scoped>
	.content {
		text-align: center;
		height: 100%;
		display: flex;
		flex-direction: column;

		.image {
			width: 100%;
			flex: 1;

			>image {
				height: 100%;
				width: 100%;
			}
		}

		.footer-button {
			display: flex;
			margin: 30rpx;
		}
	}
</style>
