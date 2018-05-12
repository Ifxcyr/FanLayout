## 可定制性超强的圆弧滑动组件
### 效果图：
![preview](https://github.com/wuyr/FanLayout/raw/master/previews/preview1.gif) ![preview](https://github.com/wuyr/FanLayout/raw/master/previews/preview2.gif) ![preview](https://github.com/wuyr/FanLayout/raw/master/previews/preview3.gif)
![preview](https://github.com/wuyr/FanLayout/raw/master/previews/preview4.gif) ![preview](https://github.com/wuyr/FanLayout/raw/master/previews/preview5.gif) ![preview](https://github.com/wuyr/FanLayout/raw/master/previews/preview6.gif)
![preview](https://github.com/wuyr/FanLayout/raw/master/previews/preview7.gif) ![preview](https://github.com/wuyr/FanLayout/raw/master/previews/preview8.gif) ![preview](https://github.com/wuyr/FanLayout/raw/master/previews/preview9.gif)
![preview](https://github.com/wuyr/FanLayout/raw/master/previews/preview10.gif)  
### 添加依赖：
build.gradle:
```
allprojects {
    repositories {
        jcenter()
        maven { url "https://github.com/Ifxcyr/FanLayout/raw/master" }
    }
}
```
app/build.gradle:
```
implementation 'com.wuyr:fanlayout:1.0.0'
```
## [查看文档](https://github.com/Ifxcyr/FanLayout/raw/master/Doc/com/wuyr/fanlayout/FanLayout.html)
### Demo: https://github.com/wuyr/FanLayout
### APIs：
```
setAutoSelect(boolean isAutoSelect)
设置当FanLayout滚动完之后，是否自动选中最近的Item


setBearingCanRoll(boolean isBearingCanRoll)
设置轴承是否可以跟随Item旋转 当 BearingType = TYPE_VIEW 时有效


setBearingColor(int color)
设置轴承颜色 当 BearingType = TYPE_VIEW 时有效


setBearingLayoutId(int layoutId)
指定轴承的布局id 当 BearingType = TYPE_VIEW 时需设置


setBearingOffset(int centerOffset)
设置轴承的偏移量


setBearingOnBottom(boolean isBearingOnBottom)
设置轴承是否在底部


setBearingType(int type)
设置轴承类型


setFixingAnimationDuration(int duration)
设置惯性滚动后，自动选中的动画时长


setGravity(int gravity)
设置对齐方式


setItemAddDirection(int direction)
设置Item的添加方向 默认: 顺时针添加


setItemAngleOffset(float angle)
指定Item的偏移角度 当LayoutMode = MODE_FIXED 时有效


setItemDirectionFixed(boolean isFixed)
设置item是否保持垂直


setItemLayoutMode(int layoutMode)
item的布局方式: 默认: MODE_AVERAGE(平均) 如设置为MODE_FIXED 需指定偏移的角度: setItemAngleOffset(float angle)


setItemOffset(int itemOffset)
设置Item的偏移量


setRadius(int radius)
指定轴承半径 当 BearingType = TYPE_COLOR 时有效


setScrollAvailabilityRatio(float ratio)
VelocityTracker的惯性滚动利用率 数值越大，惯性滚动的动画时间越长


setSelection(int index, boolean isSmooth)
选中指定的item
```
## 几行代码实现Android弧形滑动 https://github.com/Ifxcyr/ArcSlidingHelper