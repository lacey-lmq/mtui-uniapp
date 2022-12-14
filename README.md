#### 在使用 MtUI UNI版 前，请确保你已经学习并熟练使用过 [uni-app](https://uniapp.dcloud.io/) 。

### [mtui-uni 文档](https://static-ab398308-a8d9-41bf-9e5e-0129499ef255.bspapp.com/#/)
***

#
### 方式一 ：通过 npm 安装

#### 使通过 npm 安装，需要先通过 vue-cli 创建 uni-app 项目，[详见](https://uniapp.dcloud.io/quickstart-cli)

```bash
npm install mtui-uni --save
```

```javascript
//在 main.js 中引入组件库
import Vue from 'vue'

import mtui from "mtui-uni";
Vue.use(mtui);
```

```css
/* 在 App.vue 中引入字体图标 */
@import "mtui-uni/src/components/mt-theme/iconfont/iconfont.css";
```

```scss
//在 uni.scss 中引入组件样式
@import "mtui-uni/src/components/mt-theme/index.scss";
```


### 方式二 ：通过下载代码

#### 通过 GitHub 下载组件，将 `src/components/` `/static` 目录拷贝到自己的项目中。

```bash
git clone https://github.com/lacey-lmq/mtui-uniapp.git
```

```css
/* 在 App.vue 中引入字体图标 */
@import "mtui-uni/src/components/mt-theme/iconfont/iconfont.css";
```

```scss
//在 uni.scss 中引入组件样式
@import "./components/mt-theme/index.scss";
```


### 方式三 ：选择需要的模块引入
#### 下载 Mt UI 的代码，在 `src/components/` 目录下找到需要的组件拷贝到自己的项目中。

```bash
git clone https://github.com/lacey-lmq/mtui-uniapp.git
```

##### 在 `src/components/mt-theme` 目录下找到需要的组件样式拷贝到项目中。 

```css
/* 在 App.vue 中引入字体图标 */
@import "mtui-uni/src/components/mt-theme/iconfont/iconfont.css";
```

```scss
//在 uni.scss 中引入组件样式
@import "./components/mt-theme/mt-box.scss";
```
