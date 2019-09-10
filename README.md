# vue-better-slider

## 这是什么(What is it)
为vue提供的一个轮播图组件

## 代码演示如何使用

npm install vue-better-slider --save 

### 1.main.js引入样式文件
```js
import 'vue-better-slider/style.css'

```
### 2.导入并注册组件,注册组件
```js
import {IcSlider,IcSliderItem} from 'vue-better-slider'
components: {
   IcSlider,
   IcSliderItem
}
```
### 3.template模板
```html
   <ic-slider :autoplay="3000">
      <ic-slider-item v-for="(items,index) in images">
        <img :src="items.picUrl"/>
      </ic-slider-item>
    </ic-slider>
```

```js
  export default {
    data() {
      return {
        images: [
          {
            linkUrl: 'http://y.qq.com/w/album.html?albummid=0044K2vN1sT5mE',
            picUrl: 'http://y.gtimg.cn/music/photo_new/T003R720x288M000001YCZlY3aBifi.jpg',
            id: 11351
          },
          {
            linkUrl: 'https://y.qq.com/m/digitalbum/gold/index.html?_video=true&id=2197820&g_f=shoujijiaodian',
            picUrl: 'http://y.gtimg.cn/music/photo_new/T003R720x288M000004ckGfg3zaho0.jpg',
            id: 11372
          },
          {
            linkUrl: 'http://y.qq.com/w/album.html?albummid=001tftZs2RX1Qz',
            picUrl: 'http://y.gtimg.cn/music/photo_new/T003R720x288M00000236sfA406cmk.jpg',
            id: 11378
          },
          {
            linkUrl: 'https://y.qq.com/msa/218/0_4085.html',
            picUrl: 'http://y.gtimg.cn/music/photo_new/T003R720x288M000001s0BXx3Zxcwb.jpg',
            id: 11375
          },
          {
            linkUrl: 'https://y.qq.com/m/digitalbum/gold/index.html?_video=true&id=2195876&g_f=shoujijiaodian',
            picUrl: 'http://y.gtimg.cn/music/photo_new/T003R720x288M000002cwng4353HKz.jpg',
            id: 11287
          }
        ]
      }
    }
  }
```
## 组件演示demo

```js
git clone https://github.com/songhaoreact/vue-better-slider.git
cd vue-better-slier
npm install 
npm run dev
```

## 效果图

![image](http://oij04cgoe.bkt.clouddn.com/demo.gif)

## 说明

实现功能有：轮播 自动播放 dots 循环播放，适合手机端,图片高度自适应











