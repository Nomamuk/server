# Ratel-Online
[![Go Reference](https://pkg.go.dev/badge/github.com/ratel-online/server.svg)](https://pkg.go.dev/github.com/ratel-online/server)

命令行在线多人斗地主！支持癞子，大招，不洗牌等模式！
## 客户端
- 浏览器在线：[http://rtol.isnico.com/](http://rtol.isnico.com/)
- 客户端下载：[https://github.com/ratel-online/client/releases](https://github.com/ratel-online/client/releases)

## 社区
- QQ群：[948365095](https://jq.qq.com/?_wv=1027&k=OhGYB1EC)
## 玩法介绍
### 模式
- **Classic**: 经典版斗地主模式
- **LaiZi**: 癞子版斗地主模式
- **Skill**: 癞子版技能大招模式

### 规则
游戏人数2~6人不等，超过3人2副牌，超过5人3副牌，规则参考欢乐斗地主。

出牌时，直接输入想出的牌型，例如3~A顺子：`34567890jqka`，单10：`0`, 对2：`22`，王炸：`sx`。

癞子模式下同样，缺失的牌会自动使用癞子牌代替，例如当前牌型是``*7 6 6 5``，输入``6665``时会自动使用癞子牌``*7``来代替缺失的6。

更多例子:
- 4个10：`0000`
- 王炸：`sx`
- 3~A顺子：`34567890jqka`
- 3带1：`3334`
- 飞机：`jjjqqq34`

### 演示
视频教程：[https://www.bilibili.com/video/BV16Y411b7BD](https://www.bilibili.com/video/BV16Y411b7BD)

![demo](demo.gif)
### 指令 
全局指令：
- `v`：刷新可用房间列表/查看房间成员/查看其它玩家游戏状态
- `e`：退出/返回

房间指令：
- `s`：房间内开始游戏
- `set ds on`： 开启不洗牌模式
- `set ds off`： 关闭不洗牌模式
- `set sk on`： 开启技能模式
- `set sk off`： 关闭技能模式
- `set lz on`： 开启癞子模式
- `set lz off`： 关闭癞子模式
- `set pwd xxxx`：设置密码，例如密码为"xxxx"
- `set pwd off`：取消密码
- `set pn 6`: 设置房间人数上限，例如最大6个人
- 其余的会转为聊天内容

游戏指令：
- `p`：不出
- 其余的会转为聊天内容

## 技能大招
开启技能模式以后，玩家会随机被分配以下技能中的一个，**主回合**触发：
- **我要色色**：其余玩家沉迷其中，趁机偷掉了他们的最牛的牌
- **火眼金睛**：看穿对手的手牌
- **改换家门**：手牌重新分配
- **破斧沉舟**：只留下5张最强的牌
- **大幻想家**：最小的一张牌变成了癞子
- **两极反转**： 随机与一名玩家调换手牌
- **追亡逐北**：主回合，多获得一次出牌机会
- **时空裂缝**：其余玩家出牌时间减半
- **996**：所有对手强制获得9,9,6三张牌
- **添砖加瓦**：从弃牌池中随机抽取两张牌返还给所有对手
