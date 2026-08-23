---
title: "荣耀终端有限公司｜强化学习运动控制算法实习生"
excerpt: "独立完成元气仔 Dodgeball 强化学习运动控制算法开发，对比 FSQ-VAE 两阶段技能迁移与 AMP 端到端方案，结合 Multi-AMP、CBF 和视觉输入适配提升多方向躲避能力与动作自然度。"
collection: portfolio
date: 2026-06-01
date_display: "2026年6月"
published: true
---

<div class="project-meta">
  <div><span class="k">公司</span>荣耀终端有限公司</div>
  <div><span class="k">岗位</span>强化学习运动控制算法实习生</div>
  <div><span class="k">时间</span>2026.06 – 至今</div>
</div>

<style>
.project-meta { margin: 1em 0 1.6em; padding: 0.85em 1.1em; background: #f5f7fa; border-left: 3px solid #8aa2c8; font-size: 0.95em; line-height: 1.85; color: #555; }
.project-meta .k { display: inline-block; width: 4.5em; color: #333; font-weight: 600; }
</style>

## 项目简介

面向元气仔开发 **Dodgeball（躲避球）**全身运动控制策略，独立完成任务构建、训练流程适配、技术路线验证与算法优化。方案参考 [MimicKit](https://github.com/xbpeng/MimicKit) 和 [PAC-MAN](https://github.com/lzyang2000/perceptive_cbf_rl)。

## 技术路线

- **两阶段 Mimic：**基于 FSQ-VAE 复用预训练走跑策略，将 Dodgeball 目标作为条件变量映射到已有离散技能空间。
- **端到端 AMP：**联合优化任务奖励与动作风格奖励，任务适应性和动作效果优于两阶段方案，最终选为主方案。

## 关键优化

- **参考动作优化：**替换与任务匹配度更高的动作数据，提升全身动作的协调性与自然度。
- **Multi-AMP：**分离不同方向和类型的动作先验，缓解单方向收敛及多动作相互干扰。
- **CBF 引导：**基于球与身体的安全裕度构造连续躲避梯度，减少稀疏奖励带来的工程化调参。
- **视觉输入适配：**对齐训练状态与视觉感知信息的表达，降低输入差异对策略性能的影响。

## 项目成果

- 完成 Mimic 与 AMP 两类技术范式的对比验证，确定端到端 AMP 方案。
- 实现更加自然的多方向躲避行为，并形成面向动作先验、优化信号和感知输入的系统化调优流程。
