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
  <div><span class="k">时间</span>2026.03 – 至今</div>
</div>

<style>
.project-meta { margin: 1em 0 1.6em; padding: 0.85em 1.1em; background: #f5f7fa; border-left: 3px solid #8aa2c8; font-size: 0.95em; line-height: 1.85; color: #555; }
.project-meta .k { display: inline-block; width: 4.5em; color: #333; font-weight: 600; }
</style>

## 项目目标

自研四足机器人预研项目，核心目标是验证自研电机在机器狗产品形态下的可用性与性能边界，覆盖从结构调整、算法训练到实机部署的完整链路。

## 我的任务

- 完成自研机器狗 **URDF 建模与调整**，包括碰撞体优化、关节限位标定等。
- 搭建并适配**强化学习训练框架**，针对硬件资源约束与自研电机特性调整参数及奖励设置。
- 负责机器狗户外实机测试，覆盖**爬坡、崎岖路面、抗干扰**等场景。

## 最终效果

<div class="demo-hero">
  <video autoplay muted loop playsinline controls>
    <source src="{{ site.baseurl }}/files/portfolio/internship-quadruped-sim2real/payload.mp4" type="video/mp4">
    您的浏览器不支持 HTML5 video。
  </video>
</div>

<div class="demo-row">
  <video autoplay muted loop playsinline controls>
    <source src="{{ site.baseurl }}/files/portfolio/internship-quadruped-sim2real/force.mp4" type="video/mp4">
  </video>
  <video autoplay muted loop playsinline controls>
    <source src="{{ site.baseurl }}/files/portfolio/internship-quadruped-sim2real/rough_slope.mp4" type="video/mp4">
  </video>
</div>

<style>
.demo-hero, .demo-row { max-width: 600px; margin: 1.2em auto; }
.demo-hero video { width: 100%; height: auto; display: block; border-radius: 4px; background: #000; }
.demo-row { display: flex; justify-content: space-between; align-items: flex-start; }
.demo-row video { max-height: 480px; width: auto; height: auto; display: block; border-radius: 4px; background: #000; }
@media (max-width: 620px) {
  .demo-row { flex-wrap: wrap; justify-content: center; gap: 1em; }
  .demo-row video { max-width: 100%; max-height: none; }
}
</style>
