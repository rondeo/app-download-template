# app-download
![app-download-page](https://i.screenshot.net/ej696bn)

## Table of Contents

* [Introduction](#introduction)
* [Feature](#feature)
* [Quick Start](#quick-start)
* [环境变量](#环境变量)
* [页面信息配置](#页面信息配置)
* [License](#License)

## Introduction
App下载页面模版: 简单配置一下就能得到一个app下载页面

[⬆ Back to Top](#table-of-contents)

## Feature
- 只需简单地配置下下载链接，logo等，即可得到一个app下载页面
- 体积小，打开速度快
- 响应式布局，支持移动端，pc端
- 微信浏览器、钉钉浏览器打开时，显示在浏览器打开提示
- 安卓自动弹出下载; ios自动跳转到App store

[⬆ Back to Top](#table-of-contents)

## Quick Start

```sh
git clone $repository

yarn

# 在 data.json 配置您的app数据

yarn serve


# 构建
# 配置构建目录（设置 PUBLIC_PATH）
touch .env

vi .env

# 输入环境变量PUBLIC_PATH

yarn build
```

[⬆ Back to Top](#table-of-contents)

## 环境变量

PUBLIC_PATH: 静态资源构建目录

[⬆ Back to Top](#table-of-contents)

## 页面信息配置

修改 data.json，修改后重新执行yarn serve，即可看到效果
```javascript
{
  "title": "xx App", // 显示在头部的标题，文档标题为下载加上此title，即此处文档标题为"下载xx App"
  "logo": "https://i.screenshot.net/54qmgiy", // 显示在头部的app logo
  "app": [ // app下载配置
    {
      "platform": "Android", // 平台
      "version": "v1.0.0", // 版本
      "updateTime": "2019-01-01", // 发布日期，不填将会显示 "敬请期待"
      "downloadLink":"", // 下载链接，对于ios的app，只需上架后在此填 app store 链接即可
      "qrcode": true, // 是否显示二维码

      // 安卓图标
      "platformIcon": "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADQAAABABAMAAACn5UkPAAAAG1BMVEUAAABfvRlfvRlfvRlfvRlfvRlfvRlfvRlfvRlkC4P+AAAACHRSTlMA6pIhuRVbiHyD9QIAAAEFSURBVHgB7ZQ9TwMxDIbdpiDGQoWUsd069gTDjZxgYIQBifE2GJk611U//LPrJJde7JwyIKaKd7F1j2L7HDvQqVlFr3oCKTvrHGOnClW4Us5Zxs6+Gosv6/Px5BgFYauJee0Q7XTA70iIDpKMe0I0F2iZom1KrjnFh8/mTVrJO9EePh3y5l7G20MdUC0iXlmO9BACOoNvaSqpdrh0Wf5Eo/5eRhr19zK6ZdkEbeD3Gts7uNG5NrDAuWvET474d47A2ac54poRnJMj9+UfXQ4qDEBhbArD5jSAov4cFfarsJXGSpI+iY+C4bPcs5Dc907rUpGbEd9ozJCbEf8yHgcfJFacCdYJpVD+0W2qrN4AAAAASUVORK5CYII="
    },
    {
      "platform": "iOS",
      "version": "v1.0.0",
      "updateTime": "",
      "downloadLink": "",
      "qrcode": false,
      "platformIcon": "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADkAAAA/BAMAAACob32rAAAAIVBMVEUAAACzs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozs7P8wCOwAAAACnRSTlMAGb6OcuHzpVs+6IZEKwAAAW9JREFUeAG1lb9Lw1AQx1+som5BSyhO4hCkk1Ch2ik6OolUhY4OFZzcBKdaBNf4Y3IzNUl7f6W55DXP0vveIHhTeJ93733v3vVbI8RHGBkYY6IDCN+ICOauFpBiRHsFzHwtNUepn0xniA6Y7moHE7p2jeFUvTbS6oGp5pEoga0wbUpGEJrxkaTXe+4cvtrvVnfvYWFTMyzUpPu85J3ese7kpIbb5QLR7ZNphdUnpfO6NgZ2hbJLu49x7IoUoqp7XYZEI9sBOc7rZxEi5xJ2EI20g78ZbqLUcqYbACZuGoSYuWkQ4r6kZ4DG82mQIvXdACNRiOb/RvV7rea2Wm/vT736UvtcyQoArUZjBdGp8wKU7EE68ZWCifo+LolKZ4Kiy440MPU1WbnW6aqZgXJt8dMHMFOf2HpeAKvFR9f2L6quDV70FefDgq6Jc8KtZfrr78yzyRedbriUap8iPeaNL2yG6aJLv18Nr+1KMxze2M8fURLvee/vAC0AAAAASUVORK5CYII="
    }
  ]
}
```

[⬆ Back to Top](#table-of-contents)

## License

[MIT](./LICENSE)

[⬆ Back to Top](#table-of-contents)