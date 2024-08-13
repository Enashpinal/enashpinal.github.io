3D Card：https://uiverse.io/Smit-Prajapati/tricky-lionfish-78
## 效果展示
![录制_2024_08_13_11_50_48_809](https://github.com/user-attachments/assets/fbe39dbd-faed-4a3d-acd1-0bcdfa1e0f7a)
## 实现过程

### 第一步：HTML 结构

我们先来看看 HTML 代码。这是卡片的基本结构。

```html
<div class="parent">
  <div class="card">
      <div class="content-box">
          <span class="card-title">3D Card</span>
          <p class="card-content">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
          </p>
          <span class="see-more">See More</span>
      </div>
      <div class="date-box">
          <span class="month">JUNE</span>
          <span class="date">29</span>
      </div>
  </div>
</div>
```

1. **`.parent`**：这是最外层的容器，包裹整个卡片。用来设置透视效果，让卡片看起来更立体

2. **`.card`**：这是卡片本身的部分，里面包含了你的内容和日期。

3. **`.content-box`**：这里可以填写你的内容，包括标题和描述。

4. **`.date-box`**：这个部分用来显示你的日期。

### 第二步：最基本的CSS样式

我们要为上面这些元素添加最基础的样式。

```css
.parent {
  width: 300px; /* 卡片宽度 */
  padding: 20px; /* 内边距 */
  perspective: 1000px; /* 透视效果，值越小，效果越明显 */
}

.card {
  padding-top: 50px; /* 上边距 */
  border: 3px solid rgb(255, 255, 255); /* 白色边框 */
  background: linear-gradient(135deg, #f3f3f3 0%, #ffffff 100%); /* 渐变背景 */
  width: 100%; /* 宽度100%，填满父容器 */
  box-shadow: rgba(142, 142, 142, 0.3) 0px 30px 30px -10px; /* 阴影效果 */
  transition: all 0.5s ease-in-out; /* 过渡效果 */
}
```


- **`.parent`**：
  - `width`: 设置容器的宽度为 300 像素。
  - `padding`: 给容器添加内边距
  - `perspective`: 这个属性让可以给卡片添加深度效果，值越小，效果越明显。

- **`.card`**：
  - `padding-top`: 给卡片顶部留一点空间。
  - `border`: 给卡片添加一个白色边框。
  - `background`: 设置卡片背景
  - `box-shadow`: 添加阴影效果
  - `transition`: 过渡效果，让动画更自然。

### 第三步：鼠标悬停效果

为卡片添加光标悬停时的效果。

```css
.card:hover {
  transform: rotateY(10deg); /* 鼠标悬停时向 Y 轴旋转 */
}
```


- **`:hover`**：这是一个伪类，当鼠标悬停在卡片上时会触发。
- `transform`:  用 `rotateY(10deg)` 让卡片向右旋转 10 度

### 第四步：内容区域样式

为内容区域添加样式

```css
.content-box {
  background: rgba(4, 193, 250, 0.732); /* 半透明背景 */
  padding: 60px 25px 25px 25px; /* 上、右、下、左内边距 */
  transition: all 0.5s ease-in-out; /* 过渡效果 */
}
```


- **`.content-box`**：
  - `background`: 设置一个半透明的蓝色背景
  - `padding`: 为内容区域添加内边距

### 第五步：标题和内容样式

为标题和内容设置样式

```css
.card-title {
  color: white; /* 字体颜色为白色 */
  font-size: 25px; /* 字体大小 */
  font-weight: 900; /* 字体加粗 */
  transition: all 0.5s ease-in-out; /* 过渡效果 */
}

.card-content {
  margin-top: 10px; /* 上外边距 */
  font-size: 12px; /* 字体大小 */
  color: #f2f2f2; /* 字体颜色 */
}
```


- **`.card-title`**：
  - `color`: 字体颜色为白色
  - `font-size`: 字体大小设置为 25 像素。
  - `font-weight`: 加粗字体

- **`.card-content`**：
  - `margin-top`: 在内容和标题之间留一点空间
  - `font-size`: 设置内容的字体大小
  - `color`: 设置内容的字体颜色为浅灰色

### 第六步：日期框样式

为显示日期的小方框添加样式

```css
.date-box {
  position: absolute; /* 绝对定位 */
  top: 30px; /* 距离上边 30 像素 */
  right: 30px; /* 距离右边 30 像素 */
  background: white; /* 背景颜色为白色 */
  padding: 10px; /* 内边距 */
  box-shadow: rgba(100, 100, 111, 0.2) 0px 17px 10px -10px; /* 阴影效果 */
}
```


- **`.date-box`**：
  - `position: absolute`: 让日期框相对于卡片的位置固定不变
  - `top` 和 `right`: 定位日期框的位置，让它总是显示在卡片的右上角。
  - `background`: 背景为白色
  - `box-shadow`: 为方框添加阴影效果

### 第七步：交互效果

为 "See More" 链接添加样式，你可以修改按钮上的文字。

```css
.see-more {
  cursor: pointer; /* 鼠标悬停切换光标为pointer */
  font-weight: 900; /* 字体加粗 */
  color: rgb(7, 185, 255); /* 字体颜色 */
  background: white; /* 背景颜色 */
  padding: 0.5rem 0.7rem; /* 内边距 */
  transition: all 0.5s ease-in-out; /* 过渡效果 */
}
```


- **`.see-more`**：
  - `cursor: pointer`: 鼠标悬停时显示为pointer
  - `font-weight`: 加粗字体
  - `color`: 字体颜色设定为亮蓝色
  - `background`: 背景为白色
  - `padding`: 添加内边距


## 完整代码
### HTML
```html
/* From Uiverse.io by Smit-Prajapati */ 
<div class="parent">
  <div class="card">
      <div class="content-box">
          <span class="card-title">3D Card</span>
          <p class="card-content">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
          </p>
          <span class="see-more">See More</span>
      </div>
      <div class="date-box">
          <span class="month">JUNE</span>
          <span class="date">29</span>
      </div>
  </div>
</div>
```
### CSS
```css
/* From Uiverse.io by Smit-Prajapati */ 
.parent {
  width: 300px;
  padding: 20px;
  perspective: 1000px;
}

.card {
  padding-top: 50px;
  /* border-radius: 10px; */
  border: 3px solid rgb(255, 255, 255);
  transform-style: preserve-3d;
  background: linear-gradient(135deg,#0000 18.75%,#f3f3f3 0 31.25%,#0000 0),
      repeating-linear-gradient(45deg,#f3f3f3 -6.25% 6.25%,#ffffff 0 18.75%);
  background-size: 60px 60px;
  background-position: 0 0, 0 0;
  background-color: #f0f0f0;
  width: 100%;
  box-shadow: rgba(142, 142, 142, 0.3) 0px 30px 30px -10px;
  transition: all 0.5s ease-in-out;
}

.card:hover {
  background-position: -100px 100px, -100px 100px;
  transform: rotate3d(0.5, 1, 0, 30deg);
}

.content-box {
  background: rgba(4, 193, 250, 0.732);
  /* border-radius: 10px 100px 10px 10px; */
  transition: all 0.5s ease-in-out;
  padding: 60px 25px 25px 25px;
  transform-style: preserve-3d;
}

.content-box .card-title {
  display: inline-block;
  color: white;
  font-size: 25px;
  font-weight: 900;
  transition: all 0.5s ease-in-out;
  transform: translate3d(0px, 0px, 50px);
}

.content-box .card-title:hover {
  transform: translate3d(0px, 0px, 60px);
}

.content-box .card-content {
  margin-top: 10px;
  font-size: 12px;
  font-weight: 700;
  color: #f2f2f2;
  transition: all 0.5s ease-in-out;
  transform: translate3d(0px, 0px, 30px);
}

.content-box .card-content:hover {
  transform: translate3d(0px, 0px, 60px);
}

.content-box .see-more {
  cursor: pointer;
  margin-top: 1rem;
  display: inline-block;
  font-weight: 900;
  font-size: 9px;
  text-transform: uppercase;
  color: rgb(7, 185, 255);
  /* border-radius: 5px; */
  background: white;
  padding: 0.5rem 0.7rem;
  transition: all 0.5s ease-in-out;
  transform: translate3d(0px, 0px, 20px);
}

.content-box .see-more:hover {
  transform: translate3d(0px, 0px, 60px);
}

.date-box {
  position: absolute;
  top: 30px;
  right: 30px;
  height: 60px;
  width: 60px;
  background: white;
  border: 1px solid rgb(7, 185, 255);
  /* border-radius: 10px; */
  padding: 10px;
  transform: translate3d(0px, 0px, 80px);
  box-shadow: rgba(100, 100, 111, 0.2) 0px 17px 10px -10px;
}

.date-box span {
  display: block;
  text-align: center;
}

.date-box .month {
  color: rgb(4, 193, 250);
  font-size: 9px;
  font-weight: 700;
}

.date-box .date {
  font-size: 20px;
  font-weight: 900;
  color: rgb(4, 193, 250);
}
 
```