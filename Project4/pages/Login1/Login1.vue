<template>
	<view class="content">
		<view class="box">
			<input class="input1" type="text" value="" placeholder="请输入手机号码" />
			<input class="input2" type="password" value="" placeholder="请输入密码" />
			<text class="text1">忘记密码？</text>
			<text class="text2" v-on:click="zhuce">去注册</text>
			<view class="btn">
				登录
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {
			zhuce(){
				// console.log(123);
				uni.navigateTo({
					url: '/pages/zhuce/zhuce1',
				});
			}
		}
	}
</script>

<style>
	uni-page-body,
	.content {
		background-color: rgb(15, 174, 255);
		position: relative;
		height: 100%;
		color: white;
	}
	.box {
		position: absolute;
		top: 30%;
		left: 50%;
		transform: translate(-50%, -50%);
	}

	.input1 {
		width: 500rpx;
		margin-bottom: 50rpx;
	}
	.input2{
		margin-bottom: 50rpx;
	}
	.text1{
		font-size: 28rpx;
	}
	.text2{
		font-size: 28rpx;
		margin-left: 100rpx;
	}
	.btn{
		width: 260rpx;
		height: 100rpx;
		background-color: white;
		font-size: 40rpx;
		color: rgb(15, 174, 255);
		border-radius: 50rpx;
		text-align: center;
		line-height: 50px;
		margin-top: 100rpx;
	}
</style>
