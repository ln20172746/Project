<template>
		<view class="content">
			<view class="box">
				<input type="text" placeholder="请输入手机号码" v-model="phone">
				<input type="password" placeholder="请输入密码" v-model="psw">
				<input type="password" placeholder="请再次输入密码" v-model="spsw">
				<input type="text" placeholder="请输入验证码" v-model="sure">
				<view class="btn" v-on:click="zhuce">
					注册
				</view>
			</view>
		</view>
</template>

<script>
	export default {
		data() {
			return {
				phone:'',
				psw:'',
				spsw:'',
				sure:''
			}
		},
		methods: {
			zhuce(){
				// console.log(this.phone);
				// console.log(this.psw);
				// console.log(this.spsw);
				// console.log(this.sure);
				let reg1= /^([1]\d{10}|([\(（]?0[0-9]{2,3}[）\)]?[-]?)?([2-9][0-9]{6,7})+(\-[0-9]{1,4})?)$/;
				if(this.phone==''||this.psw==''||this.spsw==''||this.sure==''){
					uni.showModal({
						title:'输入错误',
						content:'手机号码或密码不能为空'
					})
				}else{
					if(reg1.exec(this.phone)){
						if(this.psw==this.spsw){
							console.log(123);
							uni.showModal({
								title:'输入正确',
								content:'注册成功'
							})
						}else{
							uni.showModal({
								title:'输入错误',
								content:'两次密码输入不一致'
							})
						}
					}else{
						uni.showModal({
							title:'输入错误',
							content:'请输入正确的电话号码'
						})
					}
				}
			}
		}
	}
</script>

<style>
	uni-page-body,
	.content{
		background-color: rgb(15, 174, 255);
		height: 100%;
	}
	.box {
		position: absolute;
		top: 30%;
		left: 50%;
		transform: translate(-50%, -50%);
	}
	input{
		margin-bottom: 50rpx;
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
