---
title: bing在全屏壁纸上的小细节
date: 2022-07-01T03:51:32.025Z
---
edge默认的bing搜索页是我每天见到频率最高的页面，直接影响当天的工作心情，由此也收集了不少高质量壁纸。发现一个小细节：

原始的壁纸往往 因为明度、视觉冲击位置的不可控，会对页面信息元素区产生干扰，  影响可用性体验。bing搜索在页面四周增加了阴影层，减小壁纸干扰。当鼠标放到壁纸信息区时则去掉阴影，最大化呈现壁纸的表现力。

在最合适的场景做最恰当的事！

遮罩css：

```css
/* img 图片 */ 
    background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;
    height: 101%;
    margin: -1px 0px 0px -1px;
    object-fit: cover;
    padding: 0px;
    position: absolute;
    width: 101%;

/* 遮罩 */
    background-attachment: fixed;
    background-image: radial-gradient(rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 0.5) 100%), radial-gradient(rgba(0, 0, 0, 0) 33%, rgba(0, 0, 0, 0.3) 166%);
    background-position-y: 0%;
    background-repeat: no-repeat;
    background-size: cover;
    height: 100%;
    opacity: 1;
    position: absolute;
    top: 0px;
    transition: opacity 0.3s linear 0s;
    width: 100%;
```

\----

PS : 这里说的bing搜索，是edge的启动页。

 <!--StartFragment-->

<https://ntp.msn.cn/edge/ntp?locale=en&dsp=0&sp=Google&query=enterprise&startpage=1>

<!--EndFragment-->

![](images/1.jpg "加阴影，减小干扰")

![](images/2.jpg)