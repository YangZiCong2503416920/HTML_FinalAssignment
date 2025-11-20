# 广建社联 - GuangJian Students Union Portal

## 许可证 (License)

本项目属于公共领域 (Public Domain)。您可以自由地使用、修改和分发此代码，无需任何限制。

这是一个为广东建设职业技术学院（清远校区）设计的社团联合会信息门户网站原型。

## 项目简介 (Project Overview)

本项目旨在解决校园社团信息分散、难以获取的问题，为学生提供一个集中、便捷、美观的信息浏览平台。通过展示各优秀社团的风采，促进校园文化的传播与交流。

此版本为 v1.0 原型演示版，展示了基础的静态信息展示功能。

## 功能特性 (Features)

*   **社团概览**: 首页展示精选社团信息。
*   **社团列表**: 提供所有合作社团的详细列表。
*   **社团详情**: （待完善）点击列表项可查看具体社团介绍。
*   **媒体中心**: 展示社团相关的图片和音频素材。
*   **响应式设计**: 适配桌面端和移动端浏览。

## 技术栈 (Tech Stack)

*   **前端**: HTML5, CSS3, JavaScript (ES6)
*   **后端 (部署)**: Nginx
*   **部署平台**: 阿里云 ECS 实例
*   **操作系统**: Ubuntu 20.04 LTS

## 快速开始 (Quick Start)

### 1. 获取代码 (Get the Code)

克隆或下载本仓库代码到本地。

```bash
git clone https://github.com/YangZiCong2503416920/HTML_FinalAssignment.git
# 或者
# 下载 ZIP 包并解压


部署到服务器 (Deployment)
本项目为静态网站，可部署于任何支持静态文件托管的服务。


使用 Nginx 部署 (Deploying with Nginx)
将项目所有文件（index.html, featured-carousel.html, css/, media/ 等）放置于 Nginx 的网站根目录（例如 /var/www/html/）。
sudo cp -r /path/to/your/project/* /var/www/html/

确保 Nginx 配置正确，root 指向网站根目录，并设置了 index index.html;。
server {
    listen 80;
    server_name your_domain_or_ip; # 替换为你的域名或服务器IP

    root /var/www/html;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}

重启 Nginx 服务。
sudo systemctl restart nginx

确保服务器防火墙（如 ufw）和云服务商安全组（如阿里云）已开放 80 (HTTP) 端口。
在浏览器中访问你的服务器 IP 或域名即可。


项目结构 (File Structure)
HTML_FinalAssignment/
index.html            ← 首页
list.html             ← 所有社团列表页
about.html            ← 关于我们/联系方式页
featured/             ← 精选社团详情页
    huafu.html        ← 华襟汉服社
    sheying.html      ← 摄影协会
    yinyue.html       ← 音乐类社团
    huanbao.html      ← 绿科环保协会
    renwen.html       ← 文学类社团
css/
    style.css         ← 样式表
images/
    logo.png          ← 网站 Logo
    banner.jpg        ← 首页 Banner 图
    huafu.jpg         ← 华襟汉服社图片
    sheying.jpg       ← 摄影协会图片
    yinyue.jpg        ← 音乐类社团图片
    huanbao.jpg       ← 环保协会图片
    renwen.jpg        ← 文学类社团图片
    player1.jpg       ← 精选社团轮播图片
    player2.jpg       ← 精选社团轮播图片
    player3.jpg       ← 精选社团轮播图片
media/                ← 音频文件
    demo_music.mp3    ← 音乐类社团宣传文件


待办事项 (To-Do List)
实现“社团详情”模态框或独立页面。
 优化轮播图自动播放逻辑，增加暂停/播放按钮。
 添加“校区筛选”功能。
 后续版本考虑引入后端框架和数据库以支持动态内容管理和用户交互。
 
 
贡献者 (Contributors)
杨子聪 - 初始开发与设计 - [YangZC2503416920@163.com]


致谢：对本网站部署至阿里云实例提供巨大帮助的林老师