## less
    1. 变量
        - 变量选择器
```less
@className: show;
.@{className}{
    background: red;
}
```
        - 变量拼接
```less
@v1: container;
@v2: fluid;
@container-fluid: ~'@{v1}-@{v2}';
```
        - 变量计算
```less
.contain{
    width: 1px + 2px;
}
```
    1. 嵌套
```less
div{
    width: 1px;
    span{
        width: 1px;
    }
}
```
    2. 媒体查询
```less
div{
    @media (min-width: 1200px){
        width: 1px
    }
    @media (min-width: 992px) and (max-width: 1200px){
        width: 1px;
    }
}
```
    3. 混合
       1. 基本混合
```less
.center(){
    margin: 0 auto;
}
```
       2. 条件混合
```less
@vip: 1;
.color() when(@vip = 1){
    color: red;
}
```
       3. 参数混合
```less
.size(@width, @height: 20px){
    width: @width;
    height: @height;
}
```
       4. 输出带选择器的样式
```less
.backgroundColor(){
    .body{
        background-color: skyblue;
    }
}
```
       5. 嵌套混合
```less
.size(){
    .sizeBox(){
        width: 200px;
        height: 300px;
    }
    .sizeBox();
}
```
        6. less扩展
```less
.box:extend(.box1){
    width: 1px;
}
```
        7. less导入
```less
@import '文件名.后缀';
```