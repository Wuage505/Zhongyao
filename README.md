# 植物识别 - 枸杞与菊花

这是一个基于TensorFlow.js的植物识别Web应用，可以识别枸杞和菊花的图片。该应用采用纯前端实现，无需后端服务器，可以直接在浏览器中运行。

## 功能特点

- 支持图片上传和拖放功能
- 实时预览上传的图片
- 使用TensorFlow.js进行植物识别
- 显示识别结果和可信度
- 提供植物基本信息
- 完全前端实现，无需后端支持
- 响应式设计，适配各种设备

## 技术栈

- HTML5
- CSS3 (Tailwind CSS)
- JavaScript
- TensorFlow.js
- Font Awesome

## 本地运行

1. 克隆或下载本项目
2. 使用现代浏览器（如Chrome、Firefox、Edge等）直接打开`index.html`文件
3. 或者使用本地服务器运行：
   ```bash
   # 使用Python简单HTTP服务器
   python -m http.server 8000
   # 然后在浏览器中访问 http://localhost:8000
   ```

## GitHub Pages部署

1. 确保你的项目已经推送到GitHub仓库
2. 在GitHub仓库页面，点击"Settings" -> "Pages"
3. 在"Source"部分，选择"main"分支和"/root"目录
4. 点击"Save"，GitHub将自动部署你的应用
5. 部署完成后，你可以通过 `https://<your-username>.github.io/<repository-name>/` 访问你的应用

## 模型说明

本项目包含一个示例模型文件，用于演示目的。在实际使用中，你需要训练自己的模型或使用预训练模型：

1. 使用TensorFlow或Keras训练模型
2. 将模型转换为TensorFlow.js格式：
   ```bash
   tensorflowjs_converter --input_format=keras model.h5 model/
   ```
3. 替换`model/`目录下的文件

## 自定义植物类别

要添加更多植物类别：

1. 修改`index.html`中的`labels`数组
2. 更新`plantData`对象，添加新植物的信息
3. 训练支持新类别的模型并替换现有模型文件

## 浏览器兼容性

- Chrome 69+
- Firefox 62+
- Safari 11.1+
- Edge 79+

## 性能优化

1. 模型优化：使用模型量化和压缩技术减小模型体积
2. 图片预处理：在上传前压缩图片
3. 延迟加载：非关键资源延迟加载
4. 缓存策略：缓存模型文件和静态资源

## 未来计划

- 添加更多植物类别
- 优化模型性能和准确率
- 添加历史记录功能
- 实现图片对比功能
- 添加离线工作模式

## 许可证

MIT License
