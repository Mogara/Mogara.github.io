---
layout: post
title: DSL用语设计每日总结
description: 每晚总结当日会议确定的 DSL 专用语
tags: [DSL]
image:
  background: triangular.jpg
modified: 2015-02-05
---

###用语定义
专用语：在该用语和试图表达同一内容的类似的表述中，只有该用语有效。  
承接语：不表达任何意思，仅帮助人类理解和阅读语句。  
全局时机：所有角色同时触发的时机，描述时不存在“某角色的某时机”这种说法  
局部时机：不是【全局时机】的时机，“某角色的某时机”是合理描述，若未声明角色，表示技能拥有者的该时机  

###专用语：
所有O：一局游戏中所有是O的对象  
玩家：User  
角色：Player  
你：技能拥有者  
其：指代前文提到的唯一角色或前文最后提到的非“你”的角色  
E1和E2：E1、E2都是技能/效果的时机  
P1和P2：P1 AND P2  
主公：身份局中身份为主公的角色  
对手：1v1中除你外的角色  
A之后：指动作A发生过后的时间段  
第I个P：指某角色的第I个阶段P  
其他角色：非你的角色  
一名角色：任意角色  
除P外的阶段：是 NOT P 的阶段  
这些O：指代前文最近提及的一些个O  
此O：指代前文最近提及的一个O  
于O：仅处于O时可以继续执行后续语句。（O类型为时间段）

###时机声明（带"*"的是局部时机，支持局部时机的特有语法，同时解释中的时机也专指某人的时机）：
所有玩家亮出武将牌后：表示技能/效果时机为【游戏开始前亮出武将牌后】  
分发起始手牌前：表示技能/效果的时机为【游戏开始前分发起始手牌前】  
游戏开始后：表示技能/效果的时机为【游戏开始后】  
*回合开始后：表示技能/效果的时机为【回合开始后】  
*P开始后：表示技能/效果的时机为【阶段P开始后】  
*P结束后：表示技能/效果的时机为【阶段P结束后】  
*P开始前：表示技能/效果的时机为【阶段P开始前】  
通则摸牌前：表示技能/效果的时机为【通则摸牌前】  
出牌阶段空闲点：表示技能的时机为【出牌阶段的空闲时间点】  
出牌阶段空闲点限I次：表示技能的时机为【出牌阶段的空闲时间点】，限制类型：出牌阶段空闲时间点限制，次数限制I  
通则弃置前：表示技能/效果的时机为【通则弃置前】  
使用O时：表示技能/效果的时机为【使用O时】(O类型为牌)  

###逻辑用语：
若如此做：若此用语之前的效果没有执行，那么此用语之后的效果也不执行。  

###承接语：
然后  
