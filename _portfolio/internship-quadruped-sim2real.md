---
title: "卧安机器人｜自研四足机器人强化学习运动控制（实习）"
excerpt: "卧安机器人实习：负责自研四足机器人的 URDF 建模、RL 训练框架适配与户外实机测试，完成关节抖动、基座晃动、拖地等典型问题的定位与跨团队协同解决。"
collection: portfolio
date: 2026-03-01
published: true
---

<div class="project-meta">
  <div><span class="k">公司</span>卧安机器人</div>
  <div><span class="k">岗位</span>强化学习运动控制算法实习生</div>
  <div><span class="k">时间</span>2026.03 – 2026.05</div>
</div>

<style>
.project-meta { margin: 1em 0 1.6em; padding: 0.85em 1.1em; background: #f5f7fa; border-left: 3px solid #8aa2c8; font-size: 0.95em; line-height: 1.85; color: #555; }
.project-meta .k { display: inline-block; width: 4.5em; color: #333; font-weight: 600; }
</style>

## 项目目标

自研四足机器人预研项目，核心目标是验证自研电机在机器狗产品形态下的可用性与性能边界，覆盖从结构调整、算法训练到实机部署的完整链路。

## 我的任务

- 完成自研机器狗 URDF 建模与调整，包括碰撞体优化、关节限位标定等。
- 搭建并适配强化学习训练框架，针对硬件资源约束与自研电机特性调整参数及奖励设置。
- 负责机器狗户外实机测试，覆盖爬坡、崎岖路面、抗干扰等场景。

## 解决的问题

### 问题 1：初次部署出现关节剧烈抖动

训练策略首次部署到实机后，关节出现明显抖动，单靠调整训练参数无法消除。排除策略侧因素后，调研了可售机器狗产品的公开电机参数，定位根因在于**自研电机减速比偏大**；与电机控制团队沟通确认后，推动**将关节减速比同量级下调**（实际硬件参数调整由电机团队执行）。调整后抖动消除，模型可在实机稳定运行。

### 问题 2：机身基座晃动明显，姿态不稳

实机测试中机器狗基座晃动显著，整体姿态稳定性差。在仿真中复现了同一现象后，分析结构参数确认问题来自几何构型——base 过宽、腿长偏短，运动控制余量不足。与结构团队沟通后推动"**更换更小电机 + 重新设计窄体基座**"的方案（硬件改动由结构团队完成）。新构型下机身稳定性显著提升。

### 问题 3：运动过程中足末端拖地严重

行走过程中后腿抬脚幅度不足，导致机身塌陷、足末端持续拖地。此问题属策略层面可调范围，通过迭代奖励函数并做对比实验，测试了**抬脚高度奖励**、**拖地惩罚**等多种方案。对比结果显示"**拖地惩罚**"对该问题改善最明显，调优后抬腿幅度达到预期，拖地现象消除。

## 最终效果

<!--
成功 demo（文件放到 files/portfolio/internship-quadruped-sim2real/ 下），每段用以下模板嵌入：

<video controls style="max-width: 100%; max-height: 70vh; display: block; margin: 0 auto;">
  <source src="{{ site.baseurl }}/files/portfolio/internship-quadruped-sim2real/slope.mp4" type="video/mp4">
</video>

建议清单：
- slope.mp4        户外爬坡
- rough-terrain.mp4 崎岖路面
- disturbance.mp4  抗干扰（踢 / 推）
- payload.mp4      负载行走

过程中失败 demo（建议嵌到上面对应"问题 N"小节末尾作为对比）：
- jitter-fail.mp4   问题 1 抖动现象
- base-shake.mp4    问题 2 基座晃动
- drag-fail.mp4     问题 3 拖地现象
-->

<p style="color:#888;"><em>Demo 视频待补</em></p>
