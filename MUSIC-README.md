# 背景音乐控制器 - 使用说明

## 功能概述

已为年会互动游戏网站的所有16个页面添加了背景音乐控制器，音乐可以在所有页面持续播放，并通过右下角的圆形按钮控制开关。

## 已添加的页面

| 游戏 | 文件 |
|------|------|
| 首页 | index.html |
| 谐音梗挑战 | game1-rule.html, game1-play.html, game1-result.html |
| 看emoji猜成语 | game2-rule.html, game2-play.html, game2-result.html |
| 你画我猜 | game3-rule.html, game3-setup.html, game3-play.html, game3-result.html |
| 谁是卧底 | game4-rule.html, game4-setup.html, game4-distribute.html, game4-play.html, game4-result.html |

## 使用方法

### 控制音乐播放

1. **开启音乐**：点击页面右下角的 🔇 图标
2. **关闭音乐**：点击页面右下角的 🎵 图标
3. **跨页面播放**：音乐状态会自动保存，切换页面后保持播放/暂停状态

### 视觉反馈

| 状态 | 图标 | 效果 |
|------|------|------|
| 播放中 | 🎵 | 图标旋转 + 金色脉冲波纹 |
| 已暂停 | 🔇 | 静态显示 |

## 更换音乐文件

### 方案A：使用在线音乐（推荐）

在所有HTML文件中找到以下代码：

```html
<audio id="bgMusic" loop preload="auto">
    <source src="https://music.163.com/song/media/outer/url?id=186016.mp3" type="audio/mpeg">
</audio>
```

修改 `src` 属性为其他音乐URL即可。

### 方案B：使用本地音乐文件

1. 创建 `music` 文件夹（与HTML文件同级）
2. 将音乐文件（如 `background.mp3`）放入文件夹
3. 修改所有HTML文件中的音频代码为：

```html
<audio id="bgMusic" loop preload="auto">
    <source src="./music/background.mp3" type="audio/mpeg">
</audio>
```

## 免费音乐资源推荐

### 中文音乐平台

| 平台 | 说明 |
|------|------|
| [网易云音乐](https://music.163.com) | 搜索"新年"、"喜庆"等关键词，使用歌曲外链 |
| [QQ音乐](https://y.qq.com) | 丰富的节日音乐资源 |

### 免版权音乐网站

| 网站 | 说明 |
|------|------|
| [Bensound](https://www.bensound.com) | 免费背景音乐，需注明来源 |
| [Free Music Archive](https://freemusicarchive.org) | 完全免费的原创音乐 |
| [YouTube Audio Library](https://www.youtube.com/audiolibrary) | YouTube免版权音乐库 |
| [ incompetech](https://incompetech.com) | Kevin MacLeod的免费音乐 |
| [CCMixter](https://ccmixter.org) | CC授权的音乐分享平台 |

### 推荐的年会/喜庆音乐

1. 《恭喜发财》- 陈奕迅/刘德华
2. 《新年好》- 群星
3. 《好运来》- 祖海
4. 《财神到》- 许冠杰
5. 《春节序曲》- 纯音乐

## 技术特性

- **循环播放**：音乐自动循环
- **音量控制**：默认50%音量（可修改 `MUSIC_CONFIG.volume` 调整）
- **状态持久化**：使用localStorage保存播放状态
- **浏览器兼容**：支持所有现代浏览器
- **响应式设计**：移动设备自动适配

## 常见问题

### Q: 为什么页面加载后音乐不自动播放？
A: 现代浏览器禁止自动播放音频，需要用户首次点击页面后才会开始播放。

### Q: 如何调整默认音量？
A: 修改 `MUSIC_CONFIG.volume` 的值（0.0 - 1.0）

### Q: 音乐链接失效了怎么办？
A: 建议下载音乐文件到本地，使用方案B的本地文件方式。

## 快速替换所有页面音乐

如果需要批量替换音乐，可以使用以下方法：

1. 使用代码编辑器（如VS Code）的"查找和替换"功能
2. 搜索：`https://music.163.com/song/media/outer/url?id=186016.mp3`
3. 替换为新的音乐URL
4. 选择"在所有打开的文件中替换"

---

**祝您年会顺利，游戏愉快！** 🎉
