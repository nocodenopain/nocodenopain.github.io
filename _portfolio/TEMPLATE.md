---
# ===== Project 骨架模板 =====
# 复制本文件为 short-slug.md（文件名会成为 URL 的一部分），
# 填写字段与正文后把 `published` 改成 true。

title: "项目名称"
excerpt: "一句话说明项目做了什么。可以放一张封面图：<br/><img src='/images/500x300.png'>"
collection: portfolio
date: 1970-01-01   # 占位日期，复制后替换为项目日期 YYYY-MM-DD
published: false   # 模板文件保持 false，复制后改成 true 才会出现在 Projects 页面
---

## 项目来源

<!-- 例：本项目是 XXX 实验室课题 / XXX 竞赛 / 个人兴趣项目。时间段：YYYY.MM – YYYY.MM。 -->

## 项目目的

<!-- 说明：
     1. 要解决的问题是什么；
     2. 用了什么方法 / 技术栈；
     3. 最终达到了什么指标或效果。 -->

## 视频素材

<!-- 方式一：嵌入 B 站视频（BV 号替换 BV1xxxxxxxxx） -->
<!--
<iframe src="//player.bilibili.com/player.html?bvid=BV1xxxxxxxxx&page=1&high_quality=1"
        scrolling="no" border="0" frameborder="no" framespacing="0"
        allowfullscreen="true"
        style="width: 100%; aspect-ratio: 16/9;">
</iframe>
-->

<!-- 方式二：嵌入 YouTube 视频（VIDEO_ID 替换为实际 ID） -->
<!--
<iframe src="https://www.youtube.com/embed/VIDEO_ID"
        title="YouTube video" frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
        style="width: 100%; aspect-ratio: 16/9;">
</iframe>
-->

<!-- 方式三：本地 mp4（文件放到 /files/portfolio/<项目 slug>/ 下，slug 与本 md 文件名一致） -->
<!--
<video controls style="max-width: 100%; max-height: 70vh; display: block; margin: 0 auto;">
  <source src="{{ site.baseurl }}/files/portfolio/short-slug/demo.mp4" type="video/mp4">
</video>
-->
