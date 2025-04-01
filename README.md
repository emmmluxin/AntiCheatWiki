## 关于方块人反作弊以及绕过的一些研究
---
#### 编创:

[Chen_mouse(qw_luxin_mouse)](https://space.bilibili.com/519576627){主编}

[rtdfuy(strom、5xian39)](https://space.bilibili.com/286975446){主编&润色&整理目录}

[Wxcer(Wx3er)](https://space.bilibili.com/2133991214){主编&校验}

[RqgernLQ(Astro Client Dev)](https://space.bilibili.com/1135293994){友情&内容补充}

[Mufeng](https://space.bilibili.com/604147173){友情&校验}

[0x16z](https://space.bilibili.com/3493081248696790){润色&补充&友情&校验&副编}



版本1.1.0 MouseLQ&rtd目录整理   0x16z&Mouse&Wxcer内容 Mufeng校验
Release Nightly

Wait For Add AntiCheat:Spartan、AGC、AntiCheatAddition

Wait For Update AntiCheat:Polar、Intave、Themis、Verus、Spiter

---

感谢名单:[滑稽的连](https://space.bilibili.com/1067237820)、[Upvivb](https://space.bilibili.com/1649992207)、cmd1152、[4iiiiiii2](https://space.bilibili.com/3493274998278662){liangzaihua}、[深情](https://space.bilibili.com/1500973767)、[xia__mc](https://space.bilibili.com/526612694)、[Loyisa](https://space.bilibili.com/7568442)、[GordonHim](https://space.bilibili.com/448576460) and You

---

涉及反作弊(now):
1. Vulcan 2.9.2    活跃
2. Matrix 7.11.12   活跃
3. GrimAC 2.3.68    活跃
4. NCP 3.17.1    活跃
5. Verus b3896    停更
6. Themis 0.16.1    活跃
7. Intave 12    活跃
8. Polar wdk    活跃
9. AAC 5~4    停更
10. Hawk BETA2108 BETA2008   停更  One Last Update In 2020
11. Tatako 0.96.5    活跃
12. Spiter wdk   活跃
13. Horizon-BETA17   活跃

---

## Vulcan火神:硬算、高版本弱检测、检测基岩版、付费

---

高版本弱检测两项:NoSlow(any)、Reach、Gapple(副手)、Elyra(鞘翅)、三叉戟(高版本激流:可以无限fly)

物品弱检测:Boat(船)、Wall(墙)

误判:Motion(A)[piston redstone]、Aim(Random?)、Badpacket(Random?)、speed(速度药水-II-III)、Fly(B)[Jump Boost Potions]、Elytra(?)(俯冲加速后抬头)

基岩版:有disabler可以dis掉，检测不是特别强 / Vulcan官网写"不检测"Geyser(Bedrock)事实上检测，那个官网已经非常老旧(mcplugins)

反作弊兼容服务器的版本:1.7-1.21

判断特征:拉回/回弹较少，但是GhostBlock回弹。

- Vulcan对于任何一个hack mode都具有检测项目，但是都不是很强，一般为生存服反作弊。


#### HighJump:

在不是很逆天的高度情况下在Slime/Ice(粘液块/冰块)上使用HighJump，反作弊将不会检测你(0vl)

> 测试版本1.21 Wurst

#### Scaffold:

在Expand情况下（距离较远）会不检测（isBridging = flase，且那个expand检测本来就一般）

有Raycast check,强度不高

> Edit by Wxcer.

###### Sprint:

可以进行omni(暴力的)而且没有任何bypass的情况下

虽然有sprint检测但是几乎没用

> 测试版本1.21 Wurst

#### Killaura:

Aim检测对于现代的客户端几乎没有，只要你的客户端完整修复了灵敏度即可。
Cps推荐9-12，有AutoClicker检测

可Switch，具有KeepSprint检测，不需要MoveFix，Raycast检测约等于没有，Hitbox和Reach纯属玄学。

补充：新火神新增了SpeedE，似乎是模拟但还是无法检测没Movefix的killaura。

> 测试版本1.8.9 LiquidBounce B98

#### Velocity:

中规中矩，有时候对绿玩进行轻微的误判

可以0 0（因为Vulcan对transaction的检测就是sb，cancel Transaction和velocity就可以00，虽然说改进了但是和没改进一样）

> 测试版本1.8.9 LiquidBounce B98

##### Nofall:

GroundSpoof、Vclip、Timer检测

可以使用一些客户端自带的Vulcan Nofall

建议使用安全一些的MLG

> 测试版本1.21 Wurst

##### Reach&HitBox:

在高版本根本不检测，低版本检测也几乎没有，可以使用Via or Dis

> 测试版本1.21 Wurst

##### TimerBalance(TickShift):

可以使用，但是不能特别持久，否则VL+1

> 测试版本1.21 MouseClient

#### Fly(Flight):

VulcanGhostBlock，一个很离谱的Fly方法，由于大多数人

不知道怎么激活它，所以Vulcan Dev不会修复

在用SpoofGround(FakeGround)的时候，Vulcan才会回弹(LagBack)（其实是GhostBlock检测，压根没vl）

> 测试版本1.8.9 LiquidBounce B98

---

## Matrix矩阵:硬算、高版本少量弱检测、基岩版不检测、付费、国产

---

高版本弱检测两项：Raycast(sca)、Gapple(副手)

物品弱检测:受击

误判:BadPackets(When u client lag,will get 1 timer VL)、Move(半雪groundspoof)、HitBox(高版本)-有几率吞刀

基岩版:wdk

反作弊兼容服务器的版本:idk

判断特征:有bot在你后面飘(when u get killaura VL)

- Matrix移动监测比Vulcan严重得多，大部分是由一个叫MOVE的vl担任的

#### HighJump

DamageFly，受击弱检测。

4iiiiiii2(liangzaihua)做到了很多在Matrix下的暴力绕过，有BedBreaker(Fucker)、AutoBlockKillAura等

> 暂未测试，资料来源[liangzaihua video]{https://www.bilibili.com/video/BV1rY1sY4EhN}

#### Scaffold:

有三个你值得注意的VL:
1. BLOCK:fastplace等检测
2. INTERACT:自动拿快捷栏方块检测
3. MOVE:检测sca期间是否疾跑

值得一提的是在高版本Matrix将不会检测你的rotation

并且在所有版本Matrix都有SameY+Jump弱检测

新版本矩阵已经有了抓特征的Scaffold，需要GodBridge（和Spiter类似，作者透漏过一点）

> 测试版本1.21 MouseClient <=> Via1.8.9 MouseClient，1.8.9 LiquidBounce b91

#### KillAura:

检测Strafe，转头和点击

AimBot检测有检测snap和shake，还会分析加速度，建议提前就拉好较长的swing range
而且Aim检测较强，很容易判你AimBot

Click主要监测点击速度，不超过10-14应该就没事

需要MoveFix;在LB中叫做Strafe(Strafe check)

- Click检测很是奇怪，9-12检测，10-14不检测

> 测试版本Via1.8.9 MouseClient

> 测试版本1.8.9 LiquidBounce B98

##### 新版本矩阵有一个需要加钱的云检查，且有保密协议

#### NoSlow:

有限速，可以用降速版的NoSlow，也还有另一种高级的方案:

使用类似于fastuse的，在一下子就把东西(Food)吃下去，就会超出检测

然后不检测你XD

Sword除了NCP和Blink以外都能FullMovement

> 测试版本1.20.6 LiquidBounceNextGen FastUse

> 测试版本1.21 MouseClient

#### Velocity:

中规中矩，如果使用负数Velocity可以做到0vl

其实你只要移动就可以01（Horizontal 0即可，垂直会检测）

所谓负数就是别人打你但是你的击退是向前的

> 测试版本1.21 MouseClient, 1.8.9 LiquidBounce b91

#### Reach&HitBox:

检测很严格，但是记忆中可以凭借noise range来做到3-3.3range

高版本应该是有弱检测，同时我看到过有人用VAPE做到任何range or hitbox

Hitbox误判多（当然有新的hitbox检测但是保密）

但是不知道是什么版本的了

> 测试版本1.21 MouseClient, 1.8.9 LiquidBounce b91

##### TimerBalance(TickShift):

无法使用

> 测试版本1.21 MouseClient

#### InvMove(InventoryMove):

Intave Mode即可绕过

> 测试版本1.8.9 LiquidBounce B98

#### Freeze

使用方块来自救的时候会爆INTERACT(VL)

无法替代Velocity(VL)，在Freeze时打人也叠CLICK(VL)

> 测试版本1.8.9 LiquidBounce B98

#### Timer

可降速Timer以进行Pearl/Blocks自救

> 测试版本1.8.9 LiquidBounce B98

---

## GrimAC严峻:模拟移动、高版本大量弱检测、基岩版不检测、开源免费

---

高版本弱检测:Raycast(sca)、Renge、and more

物品弱检测:Boat

误判:Simluation、BadPackets、三叉戟(高版本激流)、Elyra(鞘翅)、潜行/潜行头顶墙

基岩版:不检测

反作弊兼容服务器的版本:1.8-1.21(not have 1.7)

判断特征:回弹/跨版本没MoveFix秒ban

- GrimAC有较多的误判，也有较好的检测，他是模拟了玩家的各个移动，所以想要绕过比较难
- GrimAC会顶踢掉原版反作弊的保护，所以有一些漏洞可钻

移动类十分困难~~尽管也有人做到了Bypass Anything~~（其实是漏洞）

#### KillAura:

Rotation检测少之又少，大概只有这一个AimModulo360°

但是在开启KillAura后必须做到符合移动，这里需要开启Rotation或者

MoveFix，本人在此不过多赘述

Reach检测很严重，HitBox应该也是，所以不要拉超过3.0的Range

> 测试版本Via1.8.9 MouseClient

#### Scaffold:

在高版本检测会少很多，但是会有一个AimModulo360°

需要Bypass，然后注意一下Simluation就可以拉

strafe0.32-0.48做到bypass 6BPS

低版本的话大部分人是用Snap做到(即回头搭)

我还没有做过低版本的SCA绕过尝试

> 测试版本1.21 MouseClient

#### NoSlow:

一个是BugNoslow，又称Drop Noslow or Throw Noslow

是利用MC1.8.9的吃东西时丢出东西做到疾跑

> 未经测试

#### Velocity:

有NoXZ，即在打到对方的一瞬间进行一次Velocity，但

可能不是这个意思，我还没试过(mouse)  

不是这个意思啊

> 未经测试

#### Reach&HitBox:

上文KillAura业已提到，是很严格的，我还没见过哪个人绕了

或许TimeRange可以尝试一下

> 经验推测(LB B89)

##### TimerBalance(TickShift):

我无法使用，但是有人做到了使用

> 测试版本1.21 MouseClient

#### Blink:

使用时间只能控制在30s以内

> 未测试，经验推测

---

## NCP:硬算、高版本强检测、基岩版不清楚、开源免费

---

高版本弱检测:无

物品弱检测:无

误判:survivalfly(尤见生存服:台阶、半砖、窗户冰块)、moving.passable(
挖脚下方块，但是脚下方块实际上不能挖'类似于phase')

基岩版:听说有检测，无测试。

反作弊兼容服务器的版本:1.7-1.12 - 有更高版本的衍生反作弊

- 判断特征:回弹

- 在PVP服中比较好用，但是误判极多，有许多衍生反作弊，如UNCP\LNCP\WatchDog\WatchFrog

- NCP的服务器配置文件默认检测玩家在不完整方块即VL+1，请开启Step or don't touch

#### KillAura:

不怎么样，3.99RangeKillAura，AutoBlock就算拉Packet也没关系

> 测试版本1.8.9 FDP B9(=LB B98)

#### Scaffold:

有四项值得注意的检测:
1. FastPlace
2. blockplace.scaffold:Rotate/Angle
3. blockinteract.direction
4. moving.survivalfly

FastPlace在你斜上搭的时候会叠出vl，我还没解决方案

direction是Raycast检测，请打开你的rotation，同时检测方块锁死。  

> 检测的是玩家发c08的direction和服务器基于转头计算的direction是否相同，有误判(Xia__mc语)

survivalfly是当你在速度太快的时候有概率检测你walkspeed+vdistrel+vacc+hspeed+airjump
减速(比如说关闭sprint or 开启slow)即可

blockplace.scaffold：启发式检测，需要eagle降速绕过。

> 测试版本1.8.9 FDP B9(=LB B98)

#### NoSlow:

有NCP和UNCP的Sword Full NoSlow，但是没有Consume(Food?) NoSlow

吃东西noslow是很难去bypass的，就算在绿玩下跳着吃东西也会被反作弊打断

- loyisa的问题，可以去anticheat-test测试(Xia__mc语)

2024/12/24，BlockSMC SwordFullNoSlow(UNCP)失效

> 测试版本1.8.9 FDP B9(=LB B98)

#### Velocity:

Very Poor. 你能拉0 0然后一点事情没有

> 测试版本1.21 WurstClient

#### Reach&HitBox:

Reach在正常情况下最远距离应该是3.99Range 0vl

HitBox可以0.4 expand。

> 测试版本1.21.1 Wurst

##### TimerBalance(TickShift):

可以使用，时间不能太长，否则VL+1

> 测试版本1.21 MouseClient

#### NoFall

除Cancel、LAAC、AAC、VulcanFast288、Spartan外均可用

个人推荐Blink or MLG(items)

> 测试版本1.8.9 FDP B9(=LB B98)

---

## Verus:硬算、高版本强检、基岩版未知、付费

---

高版本弱检测:

物品弱检测:

误判:

基岩版:

反作弊兼容服务器的版本:1.7-1.20.1

- 有人说他是圈钱反作弊，但是他和Polar反作弊是同一个Dev(lucky)，估计这个反写着玩的
- 云检测，一些检测会时不时的掉
- 纯数据包，自写收发包，可能炸。

#### Velocity

velocity只检测00，拉1%就行

> 测试版本1.8.9 LiquidBounce B98 / 在云检测未掉时

---

## Themis:硬算、高版本强检、基岩版反作弊、免费

---

高版本弱检测:无

物品弱检测:wdk

误判:BadPackets、Timer、Reach(bow)

基岩版:专攻

反作弊兼容服务器的版本:1.17-1.21

- 基岩版反作弊，旧版有内存泄漏问题，新版没这个问题，战斗类检测极少
- 回弹类反作弊，能和谐GrimSpeed，GrimBoatJump之类，LagBack+++也很能误判

我不想给这个反作弊过多赘述，他只有移动类的检测，战斗类是条狗都能绕

---

## Intave

---

高版本弱检测:idk

物品弱检测:idk

误判:sword block(on u start jump)[MOVING/Celerity]、u get super kb(MOVING/Flight)、NETWORK、MOVING / Flight(在不允许放方块的地方在脚底下垫方块)

基岩版:不检测

反作弊兼容服务器的版本:idk

- Intave12/比较老的版本了Loyisa，所以本章节有十分多纰漏，反作弊有保密协议

#### KillAura

需要MoveFix，如果KillAura不打人，你需要在Target中勾选Dead(已死的实体)

有个NoSwing检测让我有点摸不着脑，可SwordBlockPacket Mode

> 测试版本1.8.9 LiquidBounce B98

#### NoSlow

不检测在灵魂沙(soulsand)上的noslow，如果检测到FoodNoSlow会切物品

Sword疑似不检测，ConsumeMode(Food、Drink)只要不是AAC5或InvalidC08就行

Bow同ConsumeMode

> 测试版本1.8.9 LiquidBounce B98

---

## Polar

---

高版本弱检测:idk

物品弱检测:idk

误判:

基岩版:不检测

反作弊兼容服务器的版本:idk

- 本Wiki不对Polar反作弊有任何描述，反作弊有保密协议

---

## AAC:

---

反作弊兼容服务器的版本:1.8.X-1.16.X

---

## Hawk:硬算、无法使用高版本、基岩版不检测、免费  `write by 0x16z&Wxcer`

高版本无法使用(误判)

物品弱检测:wdk

误判:Strafe(water)、Velocity(在墙旁边)、Speed(ice)

基岩版:不检测

- 2020年的反作弊，仅有1.8.9、1.7.10两个服务器支持版本，十分强大，误判也十分多
- Hawk默认很多检测不开，几个vl才会有一个alert，config可以调整。

#### KillAura:

Range:3.19不检测
- 在DBC时会有fightspeed VL
- 检测实际上很严格（HeuristicAim），需要拉低rotationSpeed，但是默认不开很多检测

> 测试版本1.8.9 FDPXReborn5.8.1

#### NoSlow:

Sword使用switch / Item(Food)使用Bug

> 测试版本1.8.9 FDPXReborn5.8.1

#### Velocity

硬检查

> 测试版本1.8.9 FDPXReborn5.8.1

##### BadPackets

不检查

> 测试版本1.8.9 FDPXReborn5.8.1

#### Scaffold

只有右键速度限制和弱interact检查

当右键CPS过高时，会导致VL++++

> 测试版本1.8.9 FDPXReborn5.8.1

#### INV

仅有ChestAura和MoveClick检查
MoveClick只会在Chest(箱子)内检查，在Inventory(背包)内就不会

> 测试版本1.8.9 FDPXReborn5.8.1

#### Speed

使用IntaveTimer,会有少量VL

> 测试版本1.8.9 FDPXReborn5.8.1

---

## Spiter:硬算、高版本误判、基岩版未知、付费、国产

高版本弱检测:

物品弱检测:

基岩版:wdk

#### 反作弊有保密协议，只有一些公开的内容。

#### Killaura
国内权威的机器学习，据说可以检测Augustus。但是有保密协议所以不知道具体情况。

---

## Tatako:硬算、高版本误判、基岩版不检测、免费、国产
Medusa based.  支持GeyserMC，不检测基岩版。

高版本弱检测: 暂时无  
高版本兼容：不兼容服务端，最高1.13。客户端支持Viaversion并更新兼容性但是依旧有大量的超级误判。

物品弱检测:Piston(站在活塞上即可)、Slime(粘液块:取消speed、fly check)、OnGround

误判:BalanceTimerCheck(BadPackets)、GhostBlock(FlyB)、aimF(InstantRotation)、Scaffold(限速)、Reach、flyC(groundspoof)、AuraA、BlockSprint、Bed(在床上)

- Move检测完全，但是每一项检测都是狗屎，Ymotion检测严格但误判不少
- FlyB已经重写，但是仍然有不少误判（对transaction处理不好）

> 哪个入乱写Dev的，plugin.yml不会看看？DEV：tjshawa

基岩版:不检测

#### KillAura:

强检测，有机器学习（但是有一些误判和绕过），免费客户端基本都死（有些可能死的慢，可能能活两把竞技场）  
可以试试3.1 Reach+Aimassist，不会死/死的很慢。

> 测试版本1.8.9 FDPXReborn5.8.1
> 测试版本1.8.9 LiquidBounce b91

#### NoSlow:
绕过已经修补，SpeedK

> 测试版本1.8.9 LiquidBounce b91

#### Scaffold:

开ExtraClick、KeepYJump

Raycast检测慢，有Eagle检测，如果Eagle需要将蹲下的时间随机一点。

> 测试版本1.8.9 LiquidBounce b91

#### TimerBalance(TickShift):

虽然有专项检测(BadPacket)，但是仍然可用
后来已经修补（例如LiquidBounce b91等客户端的 VulcanHop 速度，就是TimerBoost）

> 测试版本1.8.9 LiquidBounce b91

#### Speed:

IntaveTimer or strafe,speed0.3,dolaunchspeed,launchspeed0.55,uptimer0.77,downtimer1.77,resetxz(OnGround弱检测)
后Strafe被修补，不能GroundStrafe，老老实实Legit speed吧

> 测试版本1.8.9 LiquidBounce b91

#### Critical:

More Mode(NoMove)

> 测试版本1.8.9 FDPXReborn5.8.1

#### Fly:

0.95.1/Buzz   0.95.02 已经修了

久了会InvalidY，vanilla,timer0.07,speed15,motiony-0.01 已经修了

> 测试版本1.8.9 FDPXReborn5.8.1，LiquidBounce b91

#### BedBreaker:

几乎没有，跟WatchDog差不多的围绕一圈方块检查(Wall Check)  

无Raycast check

> 测试版本1.8.9 FDPXReborn5.8.1

#### Velocity:
  
不检测反向击退

> 测试版本1.8.9 FDPXReborn5.8.1

#### Strafe:

检测AirStrafe，Ground因为buffer叠不起来所以不检测，但是会检测某些AutoSprint（有缺陷）

#### NoFall:

Damage(在掉落空中受到伤害) 不检测，有人用修改的noGround绕过了（不知道思路），但大部分客户端的NoFall都用不了

#### FastUse:

没有专门的检测，但无法使用（会有杂七杂八的BadPackets）  
我也不知道能不能绕

> 测试版本1.8.9 LiquidBounce b91
---

## Horizon-BETA17

高版本弱检测:

物品弱检测:

误判:粘液块、栅栏

- 很严格 / 但是年久失修

基岩版:wdk

#### Scaffold:

检测rayCast，其他几乎不检测。

#### NoSlow:

Bug Food NoSlow / SwitchItem Sword NoSlow

#### KillAura:

BadpacketE和KillauraNormalAB为AB检测

但是仍然可以真防

---

## Grizzly

新反作弊。
物品弱检测：idk
高版本弱检测：idk
误判：idk

#### Killaura
有较好的Aim检查和一堆分析转头检查，需要RandomCenter，cps8~14，转头速度40~65  

但是新版本已经修补了FDP，LiquidBounce的Aim（实际未知）

> 测试版本1.8.9 LiquidBounce b91
#### Scaffold
有一个神奇的ScaffoldC，可能是限速，需要KeepY。

> 测试版本1.8.9 LiquidBounce b91

#### Movement
总体还可以，Speed无法绕过，检测GroundStrafe，老老实实legit speed。

> 测试版本1.8.9 LiquidBounce b91


## MX
新的战斗反作弊。只有Combat和Velocity检测。  
#### Killaura
有统计学和启发式Aimbot检测，但是检测很慢且不完全，使用低版本LB调参数和高版本LB的深度学习可以绕过。  
注意要RandomCenter和低转头速度。

> 测试版本1.8.9 LiquidBounce b91

#### Velocity
检测99% Horizontal & Vertical，且带及其恶俗的lagback。  

> 测试版本1.8.9 LiquidBounce b91

## 注释:

1. idk=i dont know=我不知道

2. wdk=we dont know=我们不知道

3. 大部分反作弊都有个共性，就是在fly的情况下(合法)再用Flight加速fly将不会被检测

> - Edit by Upvivb.

4. Raycast:视线检测，如果是方块则检测是否是你转头朝向的地方放置的，打人同理

> - Edit by Wxcer

5. 模拟移动:事实上所有反作弊本质都是模拟玩家的移动，公认的模拟移动反作弊是GrimAC、AAC、Polar、Intave

> - Edit by Wxcer

6. Swing:挥手，有歧义，比如在KillAura里面就是距离多远就开始挥刀(但是不打到)，Scaffold也是挥手，你不发Arm包可能会被检测

7. 保密协议:反作弊所拥有一项保密协议，使得反作弊不得拿来用于绕过等，一经发现会有相应处罚设施，有的反作弊保密协议限定服务器必须在多少人数以上才可使用该反作弊。

- 举例:Spiter、不允许泄露任何spiter的产品的截图，log，不允许服务器管理员查看vl信息，不允许服务器除服主以外知道spiter，不能说服务器用了spiter，必须有25+个玩家在你的服务器玩，不允许白名单服务器。  本Wiki后续可能跟进一个页面用于展示Spiter反作弊的条例全款

## 友情链接

反作弊测试服们:
1. cn.loyisa.cn (Loyisa，绝对的NO.1)
2. eu.loyisa.cn (Loyisa欧服)
3. anticheat-test.com (有一些新奇的反作弊，但是需要挂加速器)
4. tree.ac (有AAC5)
5. test.karhu.ac (Karhu测试服)
6. tatako.hezhongkj.top (tatako测试服)
7. 51.79.111.68:25612 (Grizzly测试服)




