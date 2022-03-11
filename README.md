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

# 服务器api

### 请求演示
```js
$.ajax({
     type:'POST',
     url:'https://foxpsd.com/api/shengchengtu/save/163765136915264690',
     data:JSON.stringify({
         "psd_sku":"1637737947373803488",
         "data":[
             {
              "name":"sucai",
               "content":"https://yourServer.com/1628674835625.jpg"
              },
              {
               "name":"sucai2",
               "content":"https://yourServer.com/1628671976551.jpg"
               }
           ],
           "callback":"https://yourServer.com/test"
      }),
       headers:{
           'Content-Type': 'application/json',
           //  填写你的token 进行身份识别（下面为演示token,请勿用于生产环境）
           'Authorization':'Basic xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx'
      },
      success(res){
           //操作成功
           if (res.code == '10000') {
                 console.log(res)
            }else{
                console.log(res)
           }
      },
     error(err){
           console.log(err)
      }
})
```
### 返回结果
```json
{
    "code": 10000,
    "data": {
        "success": 1,
        "msg": "操作成功",
        "sku": "1637896425191216816",
        "oss": "http://xxxxxxx.com/1637200300570/shengchengtu/20211126/163789642619938254.jpg",
        "fileName": "163789642619938254.jpg",
        "relative": "/163789642619938254.jpg",
    },
    "msg": "请求成功"
}
```









