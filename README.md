# 轻柔唤醒 · 渐强闹铃

四段原创渐强闹铃音频的静态站点，可直接部署到 GitHub Pages。

## 内容

| 文件 | 说明 |
| --- | --- |
| `index.html` | 单页站点，纯静态，无外部依赖 |
| `audio/*-5min.mp3` | 5 分钟完整版，MP3 96kbps，每段 3.4MB |
| `audio/*-38s.mp3` | 38 秒短版，用于快速试听 |
| `ringtones/*.m4r` | iOS 铃声格式，用于 iPhone 闹钟 |

## 部署到 GitHub Pages

```bash
cd site
git init -b main
git add .
git commit -m "轻柔唤醒 · 渐强闹铃"
git remote add origin git@github.com:<你的用户名>/gentle-wake-alarm.git
git push -u origin main
```

然后打开仓库 **Settings → Pages**，Source 选 **Deploy from a branch**，Branch 选 `main` / `root`，保存。
等 1 分钟左右，站点地址是：

```
https://<你的用户名>.github.io/gentle-wake-alarm/
```

## 说明

- 仓库体积约 17MB，其中音频占绝大部分。GitHub 单文件上限 100MB，Pages 站点上限 1GB，都在安全范围内。
- Pages 每月约 100GB 免费流量，按每次下载 3.4MB 算，大约能支撑 3 万次下载。
- `.nojekyll` 用来跳过 Jekyll 处理，避免以 `_` 开头的文件被忽略。
- 音频由 `tools/gen_wake.py` 合成，无版权限制，可自由使用与修改。
