# foxpsd 提供在线 api psd智能图层 Smart layer 替换


* 1.psd 解析
* 2.psd智能图层替换
* 3.psd图层扭曲
* 4.支持超大图片生成
* 5.提供在线编辑器
* 6.提供api服务
* 7.编辑器api开放

[foxpsd](https://https://foxpsd.com) 是一款功能全面的PSD源文件处理工具,该软件可以提供api接口一键批量处理photoshop生成的jpg文件,生成产品实时预览图，商品刊登图、商品生产图
https://https://foxpsd.com
![avatar](https://img.foxpsd.com/github_index.png)
![avatar](https://img.foxpsd.com/github_bianjiq.png)

https://https://foxpsd.com

# 浏览器SDK


### 实例化
```js
<script src="https://img.foxpsd.com/foxpsd-1.0.0.js"></script>

let foxpsdObj = new foxpsd("xiaoguotu", {
		psdSkus: ['1637653018199421773', '1637653008897318635'],
		goodsSku: '163765136915264690',
		token: 'Basic xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx',
                onload:function(){
                    //加载完成后的操作
                 }
	})
```
### 实例化方法
```js
<script src="https://img.foxpsd.com/foxpsd-1.0.0.js"></script>

let foxpsdObj = new foxpsd("xiaoguotu", {
		psdSkus: ['1637653018199421773', '1637653008897318635'],
		goodsSku: '163765136915264690',
		token: 'Basic xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx',
                onload:function(){
                    //加载完成后的操作
                 }
	})
       if (foxpsdObj && foxpsdObj.load) {
		foxpsdObj.command({
			image: 'https://foxpsd.com/www/images/th3.jpg',
			//传多个表示替换多个图层，使用英文逗号隔开
			layers: 'zhengmian,sucai,qianpian,右袖'
		})
	}
```

演示链接 https://img.foxpsd.com/foxpsd_demo.html



