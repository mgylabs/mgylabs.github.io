---
date: 2020-04-17 19:26:40
layout: post
title: Mulgyeol Labs Fabric Bot
subtitle: Mulgyeol Labs GitLab Bot, Developed by Mycroft
description: Mulgyeol Labs GitLab Bot, Developed by Mycroft
image: https://res.cloudinary.com/dm7h7e8xj/image/upload/v1559820489/js-code_n83m7a.jpg
optimized_image: https://res.cloudinary.com/dm7h7e8xj/image/upload/c_scale,w_380/v1559820489/js-code_n83m7a.jpg
category: code
tags:
  - python
  - bot
author: MycroftKang
---

# Auto Merge


<div class="warning">
  <p><strong>Warning!</strong></p>
  <p>Mulgyeol Labs 네임스페이스에 프로젝트를 생성하면, Shared project로 인식되어, <code>Developer</code>는 <code>master</code> 브랜치에 직접 push 할 수 없습니다.</p>
</div>

<div class="tip">
  <p><strong>Tip!</strong></p>
  <p><code>Developer</code>는 브랜치를 생성하여, 해당 브랜치로 <a href="https://backlog.com/git-tutorial/kr/stepup/stepup2_3.html">체크아웃</a> 한 후 변경사항을 push 할 수 있습니다.</p>
</div>

<div class="tip">
  <p><strong>Tip!</strong></p>
  <p>해당 브랜치의 변경사항을 <code>master</code> 브랜치에 반영하려면, <code>Merge Request</code>를 생성해야 합니다.</p>
</div>


## 1. Merge Request 병합 요청하기
`Merge Request`에 `AutoMerge` 라벨을 추가하면,  @MGYLBot이 병합 조건을 확인하고, 조건이 만족되면, 해당 `Merge Request` 병합합니다.

@MGYLBot이 확인하는 병합 조건은 다음과 같습니다.

*  `Merge Request` 제목에 `WIP:` 접두사를 제거해야 합니다.
*  `Merge Request` 상태가 `Open`으로 되어있어야 합니다.
*  최소 한 명 이상의 `Approval`이 있어야 합니다.
*  `Merge Request`에 충돌이 없어야 합니다.

위 조건이 만족되면, @MGYLBot이 자동으로 해당 `Merge Request`를 병합합니다.  


<div class="note">
  <p><strong>Note!</strong></p>
  <p><code>Merge Request</code>에 <code>AutoMerge</code> 라벨을 제거하면, @MGYLBot은 해당 <code>Merge Request</code> 더 이상 관여하지 않습니다.</p>
</div>

## 2. Merge Request 승인하기
프로젝트 구성원은 `Merge Request`에 다음과 같은 명령어를 입력하여, `Merge Request`를 승인할 수 있습니다.

>  @MGYLBot approve this


<div class="note">
  <p><strong>Note!</strong></p>
  <p><code>Merge Request</code> 작성자의 승인은 반영되지 않습니다.</p>
</div>

<div class="warning">
  <p><strong>Warning!</strong></p>
  <p><code>AutoMerge</code> 라벨이 추가되지 않았거나, 이미 병합된 <code>Merge Request</code>에 위 명령어를 입력하면, @MGYLBot은 해당 명령을 무시합니다.</p>
</div>

<!-- <div class="note">
  <p><strong>Note!</strong></p>
  <p>Information the user should notice even if skimming</p>
</div>

<div class="tip">
  <p><strong>Tip!</strong></p>
  <p>Information the user should notice even if skimming</p>
</div>

<div class="warning">
  <p><strong>Warning!</strong></p>
  <p>Information the user should notice even if skimming</p>
</div> -->