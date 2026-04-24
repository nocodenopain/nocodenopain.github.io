---
title: "Unitree Go2 盲爬 Locomotion 全流程复现与部署"
excerpt: "在 Unitree Go2 上走通 RL locomotion 的训练到部署流程，主要做盲爬，demo 为 16 cm 楼梯攀爬。"
collection: portfolio
date: 2025-01-01
published: true
---

<div class="project-meta">
  <div><span class="k">性质</span>个人项目</div>
  <div><span class="k">平台</span>Unitree Go2</div>
  <div><span class="k">方向</span>盲爬 Locomotion（仅本体感知）</div>
</div>

<style>
.project-meta { margin: 1em 0 1.6em; padding: 0.85em 1.1em; background: #f5f7fa; border-left: 3px solid #8aa2c8; font-size: 0.95em; line-height: 1.85; color: #555; }
.project-meta .k { display: inline-block; width: 4.5em; color: #333; font-weight: 600; }
</style>

## 项目目标

在 Unitree Go2 上把 RL locomotion 从算法到实机自己过一遍，主要做**盲爬**——仅依赖本体感知，不使用外部视觉。

## 实现流程

复现 HIMLoco、MoE、CTS 等论文的 RL locomotion 算法，在 Isaac Gym + Legged-Gym + rsl_rl 下训练盲爬策略，采用大规模并行 rollout 加速收敛。训练完成后在 MuJoCo 中做 sim-to-sim 验证，之后将策略导出为 JIT，部署到 Go2 板载运行。

## 最终效果

无视觉感知条件下完成 16 cm 楼梯攀爬。

<video controls style="max-width: 100%; max-height: 70vh; display: block; margin: 0 auto;">
  <source src="{{ site.baseurl }}/files/portfolio/go2-blind-locomotion/stairs.mp4" type="video/mp4">
  您的浏览器不支持 HTML5 video。
</video>
