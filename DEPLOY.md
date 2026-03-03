# GitHub Pages 部署指南

本指南将帮助你将ESP8266 MQTT LED控制网页部署到GitHub Pages，实现免费远程访问。

## 步骤1：创建GitHub仓库

1. 登录你的GitHub账号
2. 点击右上角的「+」按钮，选择「New repository」
3. 填写仓库信息：
   - Repository name: 例如 `esp8266-mqtt-led-control`
   - Description: 可选，描述你的项目
   - 选择「Public」（公开仓库，因为GitHub Pages对公开仓库是免费的）
   - 不要勾选「Initialize this repository with a README」（因为我们已经有本地README文件）
4. 点击「Create repository」

## 步骤2：将本地仓库推送到GitHub

在Web_Code目录下执行以下命令：

```bash
# 添加远程仓库（替换为你的GitHub仓库URL）
git remote add origin https://github.com/your-username/your-repository-name.git

# 推送代码到GitHub
git push -u origin master
```

## 步骤3：启用GitHub Pages

1. 进入你的GitHub仓库页面
2. 点击「Settings」标签
3. 滚动到「GitHub Pages」部分
4. 在「Source」下拉菜单中选择「main」分支（或「master」分支，取决于你的默认分支名称）
5. 点击「Save」
6. 等待几秒钟，GitHub会生成Pages URL
7. 复制生成的URL，例如：`https://your-username.github.io/your-repository-name/`

## 步骤4：访问部署后的应用

1. 打开浏览器，访问生成的GitHub Pages URL
2. 你应该能看到ESP8266 MQTT LED控制网页
3. 点击「⚙️」按钮进入配置页面，设置你的MQTT连接参数
4. 测试连接成功后，返回主页面开始控制LED灯带

## 注意事项

- GitHub Pages部署可能需要几分钟时间生效
- 确保你的ESP8266设备已连接到互联网并订阅了相同的MQTT主题
- 对于巴法云平台，需要在巴法云官网创建设备并获取私钥
- 如果你修改了代码，只需执行 `git push` 命令即可更新部署

## 其他免费部署选项

除了GitHub Pages，你还可以考虑以下免费部署选项：

1. **Vercel**: https://vercel.com/
2. **Netlify**: https://www.netlify.com/
3. **Cloudflare Pages**: https://pages.cloudflare.com/

这些平台都提供免费的静态网站托管服务，操作流程类似。
