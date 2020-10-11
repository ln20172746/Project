<template>
	<view class="content">
		<image class="logo1" src="/static/111.jpg"></image>
		<view class="text1" v-on:click="Login1">{{title1}}</view>
		<image class="logo1" src="/static/222.jpg"></image>
		<view class="text1" v-on:click="Login2">{{title2}}</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title1: '我要找工作',
				title2: '我要招人'
			}
		},
		onLoad() {

		},
		methods: {
			Login1() {
				console.log(111);
				uni.navigateTo({
					url: '/pages/Login1/Login1',
				});

			},
			Login2() {
				uni.navigateTo({
					url: '/pages/Login1/Login2',
				});
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

	.logo1 {
		height: 400rpx;
		width: 800rpx;
		margin-top: 50rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text1 {
		background-color: rgb(15, 174, 255);
		width: 600rpx;
		height: 80rpx;
		color: white;
		font-size: 38rpx;
		text-align: center;
		line-height: 40px;
		border-radius: 10rpx;

	}
</style>
