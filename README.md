# Simplex Flow Matching · 路演页

把生成模型从**两分布传输**推广到 **K 个分布的单纯形动力学**的单页数学建模路演。

纯静态、零依赖（无 CDN、无构建步骤、字体系统回退）——克隆即用。

## 本地预览

直接双击 `index.html`，或：

```bash
python -m http.server 8000
# 打开 http://localhost:8000
```

## 部署到 GitHub Pages

```bash
git init
git add .
git commit -m "Simplex Flow Matching pitch page"
git branch -M main
git remote add origin https://github.com/<你的用户名>/<仓库名>.git
git push -u origin main
```

然后在仓库 **Settings → Pages → Source** 选择 `main` 分支 / 根目录，约一分钟后访问：

```
https://<你的用户名>.github.io/<仓库名>/
```

> `.nojekyll` 已包含，跳过 Jekyll 处理，所有文件原样发布。

## 页面结构

| Part | 内容 |
|---|---|
| 01 问题 | 成对范式的三大硬伤：两端点、K(K−1) 网络爆炸、组合运算不可表达 |
| 02 框架 | ODE / SDE / Flow Matching 四步构造（离线公式渲染） |
| 03 推广 | 单纯形坐标 c_t，三类运算 + 可交互插值演示（滑块/播放） |
| 04 方法 | x1 ≡ linear 恒等式推导、vertex 条件化、63.2% 停滞天花板 |
| 05 实验 | 共享潜变量 ground truth、动态 GIF、one-step 诊断、消融 |
| 06 指标 | closure / SW2 / progress / d_true 定义式与主对比表 |
| 07 里程碑 | 循环一致性 A→B→C→A、真实街景任务（弱光增强 / 统一分割 / 掩码条件生成） |

## 图片来源

`figures/` 内图片来自项目实验（`experiments/` 各 block 输出）与真实数据验证结果，文件名与内容的对应关系见页面图注。

- 交互演示、公式排版为纯 HTML/CSS/JS 实现
- `figures/real_applications.png`：真实街景数据上的统一弱光分割 / 弱光增强 / 掩码条件图生成
