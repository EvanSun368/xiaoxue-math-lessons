# 期末提分真题 · 小学数学讲解站

纯静态小网站：6 道期末提分真题 + 每题本地讲解视频（中文旁白 + 板书画面）。

## 如何打开

**方式一（推荐）**：用浏览器直接打开

```bash
# macOS
open index.html
# Linux
xdg-open index.html
# 或把 index.html 拖进 Chrome / Edge / Firefox
```

**方式二**：本地 HTTP 服务（避免个别浏览器限制本地视频）

```bash
cd /workspace/xiaoxue-math-site
python3 -m http.server 8765
# 浏览器打开 http://127.0.0.1:8765/
```

## 目录说明

| 文件 | 说明 |
|------|------|
| `index.html` | 首页，题目卡片导航 |
| `q1.html` … `q6.html` | 各题：题干、思路、答案、嵌入视频 |
| `videos/q1.mp4` … `q6.mp4` | 讲解视频（有声） |
| `style.css` | 样式 |
| `assets/worksheet.jpg` | 原卷照片 |
| `generate_videos.py` | 重新生成视频的脚本（可选） |

## 题目答案速查

1. 气球：36 和 49（完全平方数）
2. 铁丝：16 米（逆推）
3. 桃子：② 4（38÷6 余2，再添4）
4. 买玩具：6 只；32 只
5. 舞蹈队：增加 1 人（男生应为7）
6. 锯木头：21 分钟（7刀×3分钟）

## 重新生成视频

```bash
cd /workspace/xiaoxue-math-site
.venv/bin/python generate_videos.py
```

需要：`ffmpeg`、`edge-tts`、`pillow`（已放在 `.venv`）。
