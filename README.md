<div align="center">
  <h1>
    扩展样板 
  </h1>

  <p>
    <strong>为 Chrome、Opera 和 Firefox 创建浏览器扩展的基础。</strong>
  </p>
</div>

现在 Firefox 支持 WebExtensions，在不复制代码库的情况下为多个浏览器构建浏览器扩展/插件变得更加容易。该项目是帮助您入门的明智起点。

<div align="center">
  <a href="https://www.emailthis.me/open-source/extension-boilerplate">
    <img src="./resources/chrome-promo/large.png" alt="Extension Boilerplate">
  </a>
</div>

## 功能

<dl>
  <dt>编写一次并部署到 Chrome、Opera 和 Firefox</dt>
  <dd>
    基于 WebExtensions。它还包含一个微小的 polyfill，用于为不同浏览器公开的 API 带来统一性。
  </dd>
</dl>

<dl>
  <dt>实时加载</dt>
  <dd>
    您对 CSS、HTML 和 JS 文件的更改将立即被转发，而无需手动重新加载扩展。这最终节省了大量时间并改善了开发人员体验。
  </dd>
</dl>

<dl>
  <dt>明智的起点</dt>
  <dd>
    这带有一个基于 gulp 的工作流，可将现代ES6 JavaScript 和SCSS转换为 JS/CSS。脚本使用 Babel 转译并使用 Browserify 捆绑。Sourcemaps 可用于 JS 和 SCSS。
  </dd>
</dl>

<dl>
  <dt>图标和宣传图片的草图 (.sketch) 资产</dt>
  <dd>
    .sketch 文件包含在资源目录中。这包含将扩展程序上传到应用程序商店时所需的所有图标和促销图片。
  </dd>
</dl>

<dl>
  <dt>易于配置和扩展</dt>
  <dd>
    gulpfile 很容易理解和配置。如果您想添加其他任务或删除未使用的任务，您可以轻松调整该文件以满足您的需要。
  </dd>
</dl>

<dl>
  <dt>特定于平台和特定于环境的变量。</dt>
  <dd>
    您可能需要根据您的环境指定不同的数据变量。例如，您可能希望在开发期间使用 localhost API 端点，并在将扩展提交到应用商店后使用生产 API 端点。您可以在 `config` 目录中的 json 文件中指定此类数据。

    You can also set custom data variables based on the platform (different variable for Chrome, FF, Opera).
  </dd>
</dl>



## 安装
1. 克隆存储库 `git clone https://github.com/EmailThis/extension-boilerplate.git`
2. 执行 `npm install`
3. 执行 `npm run build`

或者，如果您想试用示例扩展，这里是下载链接。下载后，解压缩文件并使用下面提到的步骤将其加载到浏览器中。
 - [**下载Chrome扩展程序**](https://github.com/EmailThis/extension-boilerplate/releases/download/v1.0/chrome.zip)
 - [**下载Opera扩展程序**](https://github.com/EmailThis/extension-boilerplate/releases/download/v1.0/opera.zip)
 - [**下载Firefox扩展程序**](https://github.com/EmailThis/extension-boilerplate/releases/download/v1.0/firefox.zip)


##### 在 Chrome 和 Opera 中加载扩展
1. 打开 Chrome/Opera 浏览器并导航到 chrome://extensions
2. 选择“开发者模式”，然后点击“加载解压后的扩展...”
3. 从文件浏览器中，选择 `extension-boilerplate/build/chrome` 或者 (`extension-boilerplate/build/opera`)


##### 在 Firefox 中加载扩展
1. 打开 Firefox 浏览器并导航到 about:debugging
2. 单击“加载临时加载项”，然后从文件浏览器中选择 `extension-boilerplate/build/firefox`


## 发展
当您想要开始开发扩展并想要启用实时重新加载时，可以使用以下任务 -

- `npm run chrome-watch`
- `npm run opera-watch`
- `npm run firefox-watch`


## 打包
运行 `npm run dist` 为每个浏览器创建一个压缩的、生产就绪的扩展。然后您可以将其上传到应用商店。


## 要做的
- [ ] 添加对 Safari 的支持
- [x] 添加 Firefox 和 Opera 促销图片
- [x] 添加示例截图模板
- [ ] 编写使用配置变量和 JS 预处理器的指南

