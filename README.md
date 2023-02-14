# easy-dialog(APP端)
## 准备工作
- 把easy-dialog文件夹放在pages下
- 将以下配置加入到pages.json
```javascript
{
	"path": "pages/easy-dialog/easy-dialog",
	"style": {
		"app-plus": {
			"animationDuration": 200,
			"animationType": "fade-in",
			"background": "transparent",
			"backgroundColorTop": "transparent",
			"popGesture": "none",
			"scrollIndicator": false,
			"titleNView": false
		},
		"disableScroll": true
	}
}
```
## 用法
### 基本调起弹框
```
uni.navigateTo({
	url: '/pages/easy-dialog/easy-dialog'
})
```
### 自定义内容
```
uni.navigateTo({
	url: '/pages/easy-dialog/easy-dialog？content=这是自定义内容'
})
```
### 自定义标题
```
uni.navigateTo({
	url: '/pages/easy-dialog/easy-dialog？titile=这是自定义标题'
})
```
