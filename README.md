# loadmore.js
## 通过Ajax获取数据实现分页上拉加载更多

### 概述
移动端项目中经常出现商品上拉加载的需求，一方面符合用户习惯，另一方面在数据量很大的情况下避免一次加载大量数据导致页面内容加载较慢。这里的实现是一次加载数据，对数据进行分页，上拉分批次加载。这种实质上也是一次请求所有数据，所以并不适合数据量特别庞大的场景，分批次请求服务的操作会在以后实现。

### 逻辑
1. 进入页面进行一次Ajax请求，加载固定数量（pageLength）的数据到页面中；
2. 监听页面触摸事件，判断为上滑并且滑到底部的时候执行loadmore()添加更多数据到页面中；

### 变量
+ dataLength -- 请求返回的数据长度
+ pageLength -- 要求一次加载的个数
+ startX, startY -- 滑动开始的X坐标和Y坐标
+ endX, endY -- 滑动结束的X坐标和Y坐标
+ dy -- 滑动开始到结束的距离，用于判断是上滑还是下滑
+ _top -- 获取一个元素的内容垂直滚动的像素数
+ bodyH -- body的高度
+ headerH -- 内容部分顶部到文档顶部的距离
+ footerH -- 页面底部的高度
+ page --分页个数

### 说明
+ ".loading"为加载动画，推荐CSS3来写；
+ ".no-more"在没有更多数据时显示；
+ 根据自己实际情况修改loadmore.js文件
+ 依赖jQuery


轻喷，过了一遍原理，很开心，溜了溜了

