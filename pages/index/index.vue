<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<view class="button" @click="openDialog1">dialog1</view>
			<view class="button" @click="openDialog2">dialog2</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
			openDialog1() {
				uni.navigateTo({
					url: '/pages/easy-dialog/easy-dialog?content=弹窗内容，告知当前状态、信息和解决方法，描述文字尽量控制在三行内&title=标题'
				})
			},
			openDialog2() {
				uni.navigateTo({
					url: '/pages/easy-dialog/easy-dialog?content=弹窗内容，告知当前状态、信息和解决方法，描述文字尽量控制在三行内'
				})
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	
	.button {
		width: 100px;
		padding: 10px;
		background-color: #f2f2f2;
		border-radius: 5px;
		text-align: center;
		margin-bottom: 20px;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
		flex-direction: column;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
