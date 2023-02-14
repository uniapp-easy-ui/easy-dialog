<template>
	<view class="mask">
		<view class="dialog">
			<view class="title" v-if="title">
				{{title}}
			</view>
			<view :class="['content', title ? 'solid' : '']">
				{{content}}
			</view>
			<view class="dialog_ft" @click="clickHandle">
				{{buttonText}}
			</view>
		</view>
	</view>
</template>

<script>
	// easy-dialog author-snoop
	export default {
		data() {
			return {
				title: '',
				content: '这是一段文字',
				buttonText: '我知道了'
			}
		},
		onLoad({content, buttonText, title}) {
			if (content) {
				this.content = content
			}
			if (title) {
				this.title = title
			}
			if (buttonText) {
				this.buttonText = buttonText
			}
			
		},
		methods: {
			clickHandle() {
				uni.navigateBack()
			}
		}
	}
</script>


<style>
	page {
		background: transparent;
	}
</style>

<style scoped>
.title {
	padding: 32px 24px 16px;
	font-size: 17px;
	font-weight: 700;
	color: #111;
}
	
.mask {
	position: fixed;
	z-index: 1000;
	top: 0;
	right: 0;
	left: 0;
	bottom: 0;
	background: rgba(0,0,0,0.6);
}

.dialog {
	width: 320px;
	margin: 0 auto;
	position: fixed;
	z-index: 5000;
	top: 50%;
	left: 16px;
	right: 16px;
	-webkit-transform: translate(0,-50%);
	transform: translate(0,-50%);
	background-color: #fff;
	text-align: center;
	border-radius: 12px;
	overflow: hidden;
	display: -webkit-box;
	display: -webkit-flex;
	display: flex;
	-webkit-flex-direction: column;
	-webkit-box-orient: vertical;
	-webkit-box-direction: normal;
	flex-direction: column;
	max-height: 90%;
	outline: 0;
}

.content {
	border-bottom: 1px solid #ececec;
}
.solid {
	font-weight: 400!important;
	padding-top: 0!important;
	color: rgba(0,0,0,0.5)!important;
	padding: 0 24px!important;
	padding-bottom: 32px!important;
}

.content, .dialog_ft {
	text-align: center;
	padding: 16px 0;
	font-weight: 700;
	font-size: 17px;
}

.content {
	padding: 16px 24px;
}

.dialog_ft {
	color: #576b95;
}
</style>
