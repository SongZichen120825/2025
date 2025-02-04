在线体验：https://songzichen120825.github.io/2025/
# 2025 蛇年烟花祝福网页项目

## 项目概述
本项目是一个庆祝 2025 蛇年的交互式网页，结合了用户输入验证、个性化祝福展示以及烟花动画效果，为用户带来独特的新年体验。用户可以输入自己的姓名和年龄，点击按钮后将展示根据年龄定制的祝福语，同时触发绚丽的烟花表演。

## 项目结构
项目主要由一个 HTML 文件（`index.html`）构成，其中包含了 HTML 结构、CSS 样式和 JavaScript 脚本。具体结构如下：

### HTML 结构
- **控制面板**：包含用户输入框、按钮和祝福语显示区域。
  - 姓名输入框：用于输入用户的姓名。
  - 年龄输入框：用于输入用户的年龄。
  - 开始按钮：点击后触发烟花表演和祝福语显示。
  - 祝福语区域：显示根据用户年龄生成的个性化祝福语。
  - 加载提示：在祝福加载过程中显示提示信息。
  - 错误信息：显示输入验证不通过的错误信息。
- **画布区域**：使用三个 `canvas` 元素分别用于绘制背景、主烟花和文字效果。

### CSS 样式
- **基础样式**：全局重置了一些默认样式，如 `margin`、`padding` 等，并设置了页面的背景色、布局方式等。
- **控制面板样式**：设置了控制面板的背景、边框、阴影等样式，以及输入框、按钮的样式。
- **画布样式**：设置了画布的位置、层级和初始显示状态。
- **文字样式**：设置了欢迎语、祝福语、加载提示和错误信息的文字样式。

### JavaScript 脚本
- **祝福语数据**：定义了不同年龄段的祝福语数组。
- **输入验证**：通过监听输入框的 `input` 事件，实时验证用户输入的姓名和年龄是否合法，合法时启用开始按钮。
- **烟花动画**：使用面向对象的方式定义了 `Firework` 类和 `Particle` 类，实现了烟花的发射、爆炸和粒子的运动效果。
- **红包类（未完成）**：定义了 `RedEnvelope` 类，用于实现红包下落的效果，但代码未完成。

## 主要功能实现

### 输入验证
用户输入姓名和年龄后，程序会实时验证输入的合法性。姓名不能为空，年龄必须在 1 到 120 之间。只有当输入合法时，开始按钮才会启用。

### 个性化祝福
根据用户输入的年龄，程序会将用户分为儿童（0 - 17 岁）、青年（18 - 40 岁）、中年（41 - 60 岁）和老年（60 岁以上）四个年龄段，并从相应的祝福语数组中随机选取 4 条祝福语展示给用户。

### 烟花动画
点击开始按钮后，会在画布上随机生成烟花，烟花会向上发射，到达目标高度后爆炸，产生多个粒子，粒子会向不同方向运动并逐渐消失。

## 使用方法
1. 打开 `index.html` 文件，页面会显示一个控制面板，包含姓名输入框、年龄输入框和开始按钮。
2. 在姓名输入框中输入你的姓名，在年龄输入框中输入你的年龄。
3. 当输入合法时，开始按钮会变为可用状态，点击开始按钮。
4. 页面会显示根据你的年龄生成的个性化祝福语，同时在背景中展示绚丽的烟花动画。

## 注意事项
- 项目使用了 HTML5 的 `canvas` 元素，因此需要在支持 HTML5 的现代浏览器中打开。
- 由于 `RedEnvelope` 类的代码未完成，红包下落的效果可能无法正常显示。

## 后续改进方向
- 完善 `RedEnvelope` 类的代码，实现红包下落的动画效果。
- 增加更多的交互元素，如音效、动画特效等，提升用户体验。
- 优化代码结构，将 JavaScript 代码模块化，提高代码的可维护性和可扩展性。
