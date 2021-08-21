## flex布局体验

  ### 传统布局和Flex布局

  传统布局
  * 兼容性好
  * 布局繁琐
  * 局限性，不能再移动端很好的布局

  Flex布局
  * 操作方便，布局极为简单，移动端应用很广泛
  * PC 端浏览器支持情况较差
  * IE 11或更低版本，不支持或仅部分支持

  ### 建议
    1. 如果是PC端页面布局，我们还是传统布局。
    2. 如果是移动端或者不考虑兼容性问题的PC端页面布局，我们还是使用flex弹性布局

## flex布局原理

   flex 是 flexible Box 的缩写，意为"弹性布局",用来为盒状模型提供最大的灵活性
   任何一个容器都可以指定为flex布局。
   * 当我们为父盒子设置了flex属性后，子元素的float、clear和vertical-align属性将失效
   * 总结：flex布局的原理总结就是：就是通过给父盒子添加flex属性，来控制子盒子的位置和排列方式。

## flex布局父项常见属性
   
     （1）主轴和侧轴
        在flex布局中，分为主轴和侧轴两个方向，同样的叫法有行和列、x轴和y轴
        * 默认主轴的方向是x轴方向，水平向右
        * 默认侧轴的方向是y轴方向，垂直向下


     （2）flex-direction 设置主轴的方向（即项目的排列方式）
         注意：主轴和侧轴是会变化的，就看flex-direction设置睡为主轴，剩下的就是侧轴。
               而我们的子元素就是根据主轴来排列的。

  | 属性值  | 说明    |
   | --- | --- |
  | row  | 默认值从左到右（主轴为x轴）  |
  | row-reverse  | 从右到左（主轴为x轴）  |
  | column  | 从上到下（主轴为y轴）  |
  | row-reverse  | 从下到上 （主轴为y轴） |
![1.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/6ffd6a29b69c41af9e6daadd335857a9~tplv-k3u1fbpfcp-watermark.image)


![2.png](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/39331e5e789c45679c53755f811021f7~tplv-k3u1fbpfcp-watermark.image)  
  
![3.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/17660cb8a4384cb7ae1fce196bcdd8bd~tplv-k3u1fbpfcp-watermark.image)


![4.png](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/094911ea896f4daca64f66b5dfa51d2f~tplv-k3u1fbpfcp-watermark.image)



     （3） justify-content 设置主轴上子元素的排列方式
          justify-content 属性定义了项目在主轴上的排列方式
          注意：在设置justify-content属性前，一定要先确定好主轴是哪个
  | 属性值  | 说明    |
  | --- | --- |
  | flex-start  | 主轴为x轴 排列方式就是从左向右 主轴是y轴 排列方式就是从上向下  |
  | flex-end  | 主轴为x轴 排列方式就是从右向左 主轴是y轴 排列方式就是从下向上  |
  | center  | 在主轴居中对齐（主轴是x轴 水平居中 主轴是y轴 垂直居中）  |
  | space-around  | 平分剩余空间 |
  | space-between  | 先两边贴边 再平分剩余空间（重要） |
  
  
![5.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/f17d134c3701404283043e5109439ab0~tplv-k3u1fbpfcp-watermark.image)


![6.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/8f78dce75bd8499ead3e5ad187139169~tplv-k3u1fbpfcp-watermark.image)


![7.png](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/1cb7e04573d14ca6b53dfc03bab258ff~tplv-k3u1fbpfcp-watermark.image)


![8.png](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/46f502009f794b4d8e9a859b54ae01fb~tplv-k3u1fbpfcp-watermark.image)


![9.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/fd3d25eb852d4f0d8d9fdd468d00d91b~tplv-k3u1fbpfcp-watermark.image)
  

     （4） flex-wrap 设置子元素是否换行
          默认情况下，子元素都是排在一条线上的（即x轴线或者y轴线）。
          但是有时候子元素太多，我们希望子元素进行换行，这时候就需要设置flex-wrap属性了

  | 属性值  | 说明    |
   | --- | --- |
  | nowrap  | 默认值 不换行  |
  | wrap  | 换行  |
  
  
![10.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/7cebb441c8ff4c0db31c456571c7cb2a~tplv-k3u1fbpfcp-watermark.image)

      （5）align-items 设置侧轴上的子元素排列方式（单行 ）
           
  | 属性值 | 说明 |
  | --- | --- |
  | flex-start | 默认值 从上到下 |
  | flex-end | 从下到上 |
  | center | 挤在一起居中（垂直居中）|
  | stretch | 拉伸 |
  
  
![11.png](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/b66a9f426d3446c0ab44f2fb20e5935c~tplv-k3u1fbpfcp-watermark.image)


![12.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/6f464260cda04bfcbe317ba12809fac0~tplv-k3u1fbpfcp-watermark.image)


![13.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/86b2cca5dbde4c80999747b20a9a8b13~tplv-k3u1fbpfcp-watermark.image)


![14.png](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/1ccafeab43e141e9ac8d3fd0b603f37e~tplv-k3u1fbpfcp-watermark.image)

     （6）align-content 设置侧轴上的子元素的排列方式（多行）
          注意：align-content属性只能用于子项出现换行的情况下，在单行的情况下是没有效果的

  |属性值| 说明|
  | --- | --- |
  |flex-start| 默认值在侧轴的头部开始排列|
  |flex-end| 在侧轴的尾部开始排列|
  |center| 在侧轴中间显示|
  |space-around| 子项在侧轴平分剩余空间|
  |space-between| 子项在侧轴先分布在两头，再平分剩余空间|
  |stretch| 设置子项元素高度平分父元素高度 |
  
  
![15.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/62ba88be529b40988853a5ba13487c82~tplv-k3u1fbpfcp-watermark.image)

![16.png](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/f46e316707124ab59fbaeb5bfd45d87c~tplv-k3u1fbpfcp-watermark.image)


![17.png](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/b864e4520aff403480ed748954841807~tplv-k3u1fbpfcp-watermark.image)


![18.png](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/0f087988fb4b4efe80bdabb210ab52e2~tplv-k3u1fbpfcp-watermark.image)


![19.png](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/e694aa6add044ad5aa5900e019ac5c35~tplv-k3u1fbpfcp-watermark.image)

      （7）align-content 和 align-items 区别

          * align-items 适用于单行情况下， 只有上对齐、下对齐、居中和 拉伸
          * align-content 适应于换行（多行）的情况下（单行情况下无效）， 可以设置 上对齐、 下对 齐、居中、拉伸以及平均分配剩余空间等属性值。
          * 总结就是单行找 align-items 多行找 align-content

      （8）flex-flow 
           flex-flow 属性是 flex-direction 和 flex-wrap 属性的复合属性
           flex-flow:row wrap;

##  flex布局子项常见属性

    （1）flex 子项目占的份数
        flex 属性定义子项目分配剩余空间，用flex来表示占多少份数。
        .item {
          flex: <number>; /* default 0 */
        }
    （2）align-self 控制子项自己在侧轴的排列方式

        align-self 属性允许单个项目有与其他项目不一样的对齐方式，可覆盖 align-items 属性。
        默认值为 auto，表示继承父元素的 align-items 属性，如果没有父元素，则等同于 stretch。
        span:nth-child(2) {
          /* 设置自己在侧轴上的排列方式 */
          align-self: flex-end;
        }

    （3）order属性定义子项的排列顺序（前后顺序）
        数值越小，排列越靠前，默认为0。
        注意：和 z-index 不一样。
        .item {
          order: <number>;
        }
 ##  flex布局实现垂直水平居中（单行）
 
![20.png](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/c4cc8c2dba524dcc9b66177899d7444d~tplv-k3u1fbpfcp-watermark.image)

           
本文的实战项目地址：
https://github.com/dabaoRain/css-flex
作者对于css中flex弹性布局的理解属于基础入门级别，对于文章中的理解或者使用错误，望各位大神不吝指出，关于css中flex弹性布局有那些需要补充的也可以进行评论，作者不胜感激。排版码字不易，觉得对您有所帮助，就帮忙点个赞吧！
