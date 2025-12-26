我需要为年会互动游戏网站添加背景音乐功能，要求音乐可以在所有页面持续播放，并且可以控制开关。

功能要求：

1. 音乐播放特性：
   - 自动循环播放（loop）
   - 默认音量：50%（可调节）
   - 页面加载后自动播放（用户交互后开始，符合浏览器政策）
   - 跨页面持续播放（使用localStorage记录播放状态）

2. 音乐控制器UI设计：
   - 位置：固定在页面右下角
   - 样式：圆形按钮，半透明背景
   - 图标：
     * 播放状态：显示音乐图标🎵或音符图标
     * 暂停状态：显示静音图标🔇
   - 悬停效果：放大、阴影加深
   - 点击效果：切换播放/暂停状态

3. 功能实现：
   - 点击按钮切换播放/暂停
   - 使用localStorage保存播放状态（playing: true/false）
   - 页面加载时读取localStorage，恢复上次的播放状态
   - 音乐文件使用HTML5 Audio API

4. 音乐文件处理：
   - 方案A（推荐）：使用在线音乐URL
     * 示例：https://example.com/music.mp3
     * 可以使用免费音乐资源网站的直链
   - 方案B：使用本地音乐文件
     * 文件路径：./music/background.mp3
     * 需要用户自己准备音乐文件

5. 需要添加音乐控制器的页面（所有页面）：
   - index.html（首页）
   - game1-rule.html, game1-play.html, game1-result.html
   - game2-rule.html, game2-play.html, game2-result.html
   - game3-rule.html, game3-setup.html, game3-play.html, game3-result.html
   - game4-rule.html, game4-setup.html, game4-distribute.html, game4-play.html, game4-result.html

6. 代码结构：
   - 创建一个可复用的音乐控制器代码片段
   - 可以直接复制粘贴到每个HTML文件的<body>标签末尾
   - 包含HTML结构 + CSS样式 + JavaScript逻辑

样式要求：
- 音乐控制器样式：
  * 大小：60×60px圆形按钮
  * 背景：半透明黑色（rgba(0,0,0,0.6)）
  * 图标大小：30px
  * 位置：固定在右下角，距离底部和右侧各20px
  * 层级：z-index: 9999（确保在最上层）
  * 动画：旋转动画（播放时图标旋转）
- 年会风格配色（可选金色边框）

技术要求：
- 使用HTML5 Audio API
- 使用localStorage保存播放状态
- 使用CSS3动画
- 代码注释清晰
- 兼容主流浏览器

请生成以下内容：
1. 完整的音乐控制器代码片段（可直接复制到每个页面）
2. 使用说明（如何添加到现有页面）
3. 音乐文件准备指南（推荐的免费音乐资源网站）
