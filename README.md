# ESP8266 MQTT LED 控制网页

这是一个用于控制ESP8266连接的WS2812智能灯带的网页应用。

## 功能特点

- 支持简单模式和高级模式控制
- 支持多种MQTT平台：巴法云、EMQX公共服务器、Home Assistant、阿里云IoT等
- 提供系统预设效果：单色、彩虹、跑马灯、流水灯等
- 支持自定义效果编辑器
- 响应式设计，适配移动端

## 技术栈

- HTML5 + CSS3
- Vue.js 2.x
- iView UI框架
- MQTT.js

## 部署说明

### 本地部署
1. 直接在浏览器中打开 `mqtt.html` 文件
2. 或使用本地服务器（如 http-server、live-server 等）

### 远程部署（GitHub Pages）
1. 克隆此仓库到GitHub
2. 在仓库设置中启用GitHub Pages
3. 选择 `main` 分支作为源
4. 访问生成的GitHub Pages URL

## 配置说明

1. 打开 `config.html` 配置MQTT连接参数
2. 选择合适的MQTT平台并填写对应参数
3. 测试连接成功后保存配置

## 项目结构

```
├── css/           # 样式文件
├── img/           # 图片资源
├── js/            # JavaScript文件
├── config.html    # 平台配置页面
├── editor.html    # 效果编辑器页面
├── mqtt.html      # 主控制页面
└── README.md      # 项目说明
```

## 使用方法

1. 在 `config.html` 中配置MQTT连接
2. 在 `mqtt.html` 中控制LED灯带
3. 在 `editor.html` 中创建自定义效果

## 注意事项

- 确保ESP8266设备已连接到相同的MQTT主题
- 对于巴法云平台，需要在巴法云官网创建设备并获取私钥
- 公共MQTT服务器可能不稳定，建议使用私有的MQTT服务器或巴法云
