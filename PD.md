# Production Docs
## 背景
参加一个Camp，需要交作业，还有两周（1-9展示阶段成果，1-14 final展示）
## 想法
1. 基于demo或者engine，做简单的肉鸽游戏开发，主要流程：
	1. hometown：买/兑换装备和其他，NPC交代背景，升级英雄/展示英雄技能，仓库管理）
	2. 进入游戏：加载英雄数据
	3. 副本/关卡：选择奖励，进入关卡玩游戏，通关获得奖励
	4. 保存游戏：通过则自动调用API保存英雄数据，不通过不保存
2. 规划
	1. Unity开发，支持导出为多平台，本次基础目标是支持导出为web页面游戏
	2. 美术风格偏向于明亮，不要地牢黑暗风，2D或者伪3D，资源可以从itch.io或者unity官方store选择后购买
	3. 支持多人在线，需要有server端，保存玩家英雄数据，无进度保存
	4. 英雄数据交换提供基础API，购买兑换提供API
	5. Github repo：[https://github.com/CMUBA/Arcadia-game]
3. 游戏玩法
	1. [https://whimsical.com/game-flow-NDmpExQjfaPEnp9TACihZG]，相关设计，不一定遵守，初步思考
	2. 至少实现一个hero玩三个场景，10分钟左右通过获得奖励，奖励购买装备，兑换Coupon
	3. 英雄数据（确定中）
		{
						"name":"hero1",
						"level":  1,
						"class": "warrior",
						"race": "human",
						"talent": "spring" //Summer, Autumn, Winter
						"skills": = 13//需查元数据表，待讨论
						“equipments”： = {weapon, shield, armor, helm, amulet(necklace), glove, ring(left, right), boots}, load from hero contract
						“inventory": {itemid1, itemid22, itemid3, itemidx}
					}
		===========
		Skill 表格，metadata
						{  
						  "attributes": {  
							"basic": {  
							  "Agile": 1,  
							  "Attack": 2,  
							  "Health": 3,  
							  "Defense": 4  
							},  
							"branch": {  
							  "Spring": {  
								"Eagle Eye": 11,  
								"Spider Sense": 12,  
								"Lucky Strike": 13,  
								"Holy Retaliation": 14,  
								"Ultimate Seal": 15  
							  },  
							  "Summer": {  
								"Sharpen Blades": 21,  
								"Critical Strike": 22,  
								"Life Steal": 23,  
								"Fury": 24,  
								"Graceful Release": 25  
							  },  
							  "Autumn": {  
								"Sturdy Body": 31,  
								"Block": 32,  
								"Unyielding": 33,  
								"Shield of Darkness": 34,  
								"Final Defense": 35  
							  },  
							  "Winter": {  
								"Defense Mastery": 41,  
								"Blood Strike": 42,  
								"Malign": 43,  
								"Sacrifice": 44,  
								"Faith in the Holy Light": 45  
							  }  
							}  
						  }  
						}
		

## 资料
Topdown engine：[https://topdown-engine.moremountains.com/#demo]，[https://www.youtube.com/playlist?list=PLl3caEhMYxQGFQ8LA5doTSkWhP2Mx84Gx]，[https://topdown-engine-docs.moremountains.com/]，[https://topdown-engine.moremountains.com/topdown-engine-showcase]，[https://topdown-engine.moremountains.com/topdown-engine-contact]

Store：[https://assetstore.unity.com/packages/templates/systems/topdown-engine-89636]

下载：https://pan.baidu.com/s/1ETjXhA5AUPKTRG6piEO-wA
提取码:urcj

## Schedule
![](https://raw.githubusercontent.com/jhfnetboy/MarkDownImg/main/img/202412241316887.png)
