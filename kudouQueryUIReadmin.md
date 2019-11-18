# kudouUI 全局样式说明文档

## 布局
.container   设置为容器：水平方向居中，宽度不为100%，左右内边距为15px，高度没有
.container-fluid   宽度为100%的容器，没有外边距，内边距左右为15px，上下为0px，没高度

## 按钮  btn
#### 普通的按钮样式
成功 btn-succes
失败 btn-fail
警告 btn-warning
错误 btn-error
取消 btn-cancel
确认 btn-sure
默认 btn-default
危险 btn-danger
首选 btn-primary
一般信息 btn-info
百搭按钮 btn-normal
暖色按钮 btn-warm

## 渐变的按钮样式
成功 btn-succes-rgb
警告 btn-warning-rgb
错误 btn-error-rgb
取消 btn-cancel-rgb
确认 btn-sure-rgb
默认 btn-default-rgb
危险 btn-danger-rgb
首选 btn-primary-rgb
一般信息 btn-info-rgb
百搭按钮 btn-normal-rgb
暖色按钮 btn-warm-rgb

#### 伪类按钮样式
btn-hover

- 型号
大 btn-bg
小 btn-sm
中 btn-md

- 圆角按钮 btn-radius



## 表单 
## 滑块

## select选择框

## 表格 .table
.table :表示基础表格，必须在table标签中使用，带有边框的基础表格
.table-column :表示半边框
.table-striped ：表示条状表格，标体的偶数行有一定的背景颜色
.table-hover ：表示悬浮表格
.table-condensed ：表示紧缩表格
.table-border ：边框表格
.table-inverse ：背景色为黑色的表格
.table-inverse-strped ：黑色条形表格
.table-inverse-hover ：黑色悬浮样式 需要依赖.table或者.table-inverse-striped
.table-control ：表示“控制列”固定，其他列可以滚动 .table-control必须给table标签的祖级添加，而不能给父元素添加。.table-box表示 table的父容器
~~~css
.table-control{
   position:relative;
}
.table-control table>td:last-child{
   position:absolute;
   right:0;
   min-width:120px;
   text-align:center;
   box-shadow:-5px 4px 6px 1px #ccc;
}
/* 选中倒数第二列：解决内容遮罩问题 */
.table-control table>tr>td:nth-last-child(2)::before{
   content:"";
   width:120px;
}
.table-control>.table-box{
    overflow:auto;
}
~~~
.table-responsive ：移动端表格，可以有横向滚动的效果

状态表格：给tr添加类名
.success 成功
.info 通过
.warning 警告
.danger 危险
.primary 首选
.warm 暖色


## 栅格系统


## 分页 .Page
.pagination ：实现分页样式。由ul，li，a完成分页效果
.pagination-bgc ：表示带有背景颜色的分页
.pagination-noBgc ：表示没有背景颜色的分页

## 表单类

### 单选多选框样式
.circle-check 圆形选择框   .circle-check 需要给input[type=checkbox]的父元素添加
.square-check 方形选择框   .square-check 需要给input[type=checkbox]的父元素添加
~~~html
<!-- 实例代码 -->
<div class="circle-check">
    <input type="checkbox">
</div>  
<div class="square-check">
    <input type="checkbox">
</div> 
~~~

### 滑块 .sliderBar
.sliderBar-box ：表示进度条外围容器
.sliderBar ：表示 滑块的条
.sliderBar-control ：表示控制键
.sliderBar-number ：表示数字的框
~~~html
<div class="sliderBar-box">
        <div class="sliderBar">
            <div class="sliderBar-control">
                <div class="sliderBar-number">100</span>
            </div>
        </div>
    </div>   
~~~
状态
.sliderBar-success
.sliderBar-info
.sliderBar-primary
.sliderBar-error

### 开关 .switch
.switch ：开关样式的选择框，需要给input[type="checkbox" class="switch"] 才能实现效果
    - 绿色为开input=checked，灰色为关input=disable
状态
.switch-info ：蓝色为开，灰色为关
.switch-danger ：红色为开，灰色为关
.switch-warm ：橙色为开，灰色为关
.switch-primary ：蓝色为开，红色为关

### 步骤组件 .step
.step-wrap ：为外部容器，55rem
.step-full ：每个步骤容器。

### 导航 .nav
注意：导航仅仅适用于PC端应用，且只适用于静态的样式。导航中所有的样式都是给li下a标签设置的
.nav-tab ：表示像tab样式的导航条，需要依赖.nav
.nav-pills ：胶囊式的导航，需要依赖.nav
.nav-stacked ：侧边导航样式
.nav-inverse ：表示背景色为黑色的导航
.nav-inverse-stacked ：背景为黑色 经过为灰色的纵向导航
.nav-inverse-black ：横向黑色导航条，背景色为灰色，经过为黑色
.nav-inverse-grey ：灰色纵向导航条，背景色为黑色，经过为灰色

.nav-aside ：表示侧边栏的导航
.nav-fixed-top ：表示固定导航，在顶部
.nav-fixed-left ：表示屏幕左边固定导航
.nav-fixed-right ：表示屏幕右边固定导航

### 导航条 .navbar
注意：兼容移动端



## 规范：
1.清空所有HTML标签的默认样式

2.字体：标准：14px;最大：36px；最小：12px

3.布局： 栅格系统：给一个父容器，等分多少份？
    12列：
        每个子元素可以占12列中 1-12，最大为12份
        col-12:占据12份


### 表单样式组件
1.只有单纯的表单样式。分为基础样式和可选样式，如有特殊需要，请自定义。
2.表单没有进行验证处理，有对验证效果的样式处理：static 状态
3.表单验证需要JS，正则完成。注意：正则规则必须写基础规则，不要写新的正则，因为IE和火狐部分版本不兼容
#### 表单基础样式
.form-group ：表示表单组件
.form-control ：表示表单控件
.form-label ：input的提示信息，只能应用在label标签中
#### 可选项表单样式
.form-inline ：横向的表单
.form-horizontal ：纵向的表单
#### 表单中控件
.form-check ：选择项组件，在ul中使用
.form-check-item ：多选项，在li中使用
.check-content ：选择的文本描述


### 栅格系统 .col
栅格系统，是横向布局的处理
如果父容器不使用 .row,那么自己清除浮动，计算父容器高度

#### 容器 .row
将.row 容器等分为12份

#### 屏幕
.col-xs-xx  ：768以下尺寸
.col-sm-xx  :768——992
.col-md-xx  ：992——1200
.col-lg-xx  ：1200+

#### 分的份数
 1 : 8.3333333%
  2 : 16.6666667%
  3 ：25%
  4 : 33.3333333%
  5 ：41.6666667%
  6 : 50%
  7 : 58.3333333%
  8 : 66.6666667%
  9 : 75%
  10 : 83.3333333%
  11 : 91.6666667%
  12 : 100%

#### 列偏移
通过改变position:relative left实现列偏移
* 表示1 2 3 4 5 6 7 8 9 10 11 12
.col-xs-offset-*
.col-sm-offset-*
.col-md-offset-*
.col-lg-offset-*
##### 偏移量
1
2
3
4
5
6
7
8
9
10
11
12

#### 排列
.col-xs-pull-* ：相对元素位置右边多远（往左走）
.col-xs-push-* ：相对元素位置左边多远（往右走）

### 开发浏览器注意事项
1：如果您是IE7/IE8，请您更换浏览器
2：IE7尽量全使用div  例如：
    -ul div.ul
    -li div.li     
    -span div.span 设置 display:inline
3： IE7/IE8不支持浮动，清除浮动、css3百分之九十的属性