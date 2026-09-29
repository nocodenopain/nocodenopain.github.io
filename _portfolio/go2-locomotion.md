---
title: "Unitree Go2｜RL 运动控制与实机技能展示"
excerpt: "在 Unitree Go2 上做 RL 运动控制的实机落地，完成盲爬楼梯、双足倒立行走与侧空翻三项实机 demo。"
collection: portfolio
date: 2025-01-01
published: true
---

<div class="project-meta">
  <div><span class="k">平台</span>Unitree Go2</div>
  <div><span class="k">方向</span>RL 运动控制</div>
</div>

<style>
.project-meta { margin: 1em 0 1.6em; padding: 0.85em 1.1em; background: #f5f7fa; border-left: 3px solid #8aa2c8; font-size: 0.95em; line-height: 1.85; color: #555; }
.project-meta .k { display: inline-block; width: 4.5em; color: #333; font-weight: 600; }
.demo-video { margin: 1.2em auto; }
.demo-video video { width: 100%; height: auto; display: block; border-radius: 4px; background: #000; }
.demo-video.portrait { max-width: 360px; }
.demo-video.landscape { max-width: 640px; }
</style>

## 基于本地感知的运动控制

仅依赖本体感知、不使用外部视觉，完成 16 cm 连续台阶攀爬。

<div class="demo-video portrait">
  <video controls>
    <source src="{{ site.baseurl }}/files/portfolio/go2-locomotion/stairs.mp4" type="video/mp4">
    您的浏览器不支持 HTML5 video。
  </video>
</div>

## 双足倒立行走

<div class="demo-video landscape">
  <video controls>
    <source src="{{ site.baseurl }}/files/portfolio/go2-locomotion/handstand.mp4" type="video/mp4">
    您的浏览器不支持 HTML5 video。
  </video>
</div>

## 侧空翻

基于 go2_mimic 动作追踪管线：由轨迹优化生成参考动作，策略以动作追踪的方式复现该动作，实机完成侧空翻。

<div class="demo-video landscape">
  <video controls>
    <source src="{{ site.baseurl }}/files/portfolio/go2-locomotion/slideflip.mp4" type="video/mp4">
    您的浏览器不支持 HTML5 video。
  </video>
</div>
