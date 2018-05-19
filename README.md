## 可定制性超强的圆弧滑动组件
### 效果图   (表情包来源：百度贴吧)：
![preview](https://github.com/wuyr/FanLayout/raw/master/previews/1.gif) ![preview](https://github.com/wuyr/FanLayout/raw/master/previews/2.gif) ![preview](https://github.com/wuyr/FanLayout/raw/master/previews/3.gif)
![preview](https://github.com/wuyr/FanLayout/raw/master/previews/4.gif) ![preview](https://github.com/wuyr/FanLayout/raw/master/previews/5.gif) ![preview](https://github.com/wuyr/FanLayout/raw/master/previews/6.gif)
![preview](https://github.com/wuyr/FanLayout/raw/master/previews/7.gif) ![preview](https://github.com/wuyr/FanLayout/raw/master/previews/8.gif) ![preview](https://github.com/wuyr/FanLayout/raw/master/previews/9.gif)
![preview](https://github.com/wuyr/FanLayout/raw/master/previews/10.gif)
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
## [查看文档](http://htmlpreview.github.io/?https://github.com/Ifxcyr/FanLayout/blob/master/Doc/com/wuyr/fanlayout/FanLayout.html)
### Demo: https://github.com/wuyr/FanLayout
### 布局属性：
```
    <com.wuyr.FanLayout
        android:id="@+id/fan_layout"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:auto_select="true" //滚动完毕是否可以自动选中最近的item 默认: false
        app:bearing_can_roll="true" //轴承是否可以转动 默认: false
        app:bearing_color="#9F55" //轴承颜色(bearing_type=color时才有效) 默认: #000
        app:bearing_gravity="left" //对齐方式：left, right, top, bottom, left_top, left_bottom, right_top, right_bottom 默认: left
        app:bearing_layout="@layout/bearing_view" //自定义的轴承布局 (bearing_type=view时才有效)
        app:bearing_offset="0dp" //轴承偏移量
        app:bearing_on_bottom="true" //轴承是否在最底 默认: false
        app:bearing_radius="50dp" //轴承半径
        app:bearing_type="view" //轴承类型: view, color 默认: color 设置为view时需指定bearing_layout
        app:item_add_direction="clockwise" //item的添加方向:clockwise(顺时针添加), counterclockwise(逆时针), interlaced(交叉) 默认: clockwise
        app:item_angle_offset="20" //固定的偏移角度，当item_layout_mode为fixed时有效
        app:item_direction_fixed="true" //设置item是否保持垂直 默认: false
        app:item_layout_mode="average" //item的布局方式: average(平均), fixed(指定角度) 默认: average 如设置为fixed需指定item_angle_offset
        app:item_offset="0dp" //item偏移量
        />
```
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
