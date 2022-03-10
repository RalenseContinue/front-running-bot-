# 1:Front-running-bot
# 需求概述：
```
一种应用于BSC、ether的链上`全自动夹子机器人`/`抢跑机器人`（Front-running-bot）</br>
此程序可以设定相应的参数作为执行&判断条件（下文叙述）自动“检测”并执行套利的操作（应用于Uniswap & Pancakeswap的相关交易对)</br>
```
# 补充叙述：
```
1-扫描区块链并根据特定标准查找交易（待定在块上，即内存池）。它检测何时将有新的`流动性`添加到 PancakeSwap&Uniswap上的 AMM（自动做市商）池中。通过设置更高的`gas`价格同时在同一个区块下订单来进行前期（特定交易量、滑点和gas价格）交易。在`先行区块`上的买入交易完成后，在达到`特定的利润目标`后卖出！</br>
</br>
2-扫描区块链并根据特定标准查找交易（待定在块上，即内存池）它检测`现有交易对`的抢跑机会，通过设置更高的gas价格同时在同一个区块下订单来进行前期（特定交易量、滑点和gas价格）交易。在`先行区块`上的买入交易完成后，立即在`下一个区块`中卖出。</br>
```⚠️：关于补充叙述中的`1`，`2`项可以从功能门类中细分为（抢跑机器人/自动夹子机器人）两种，其中`“1”`更多倾向于全新流动性的检测，`“2”`则更倾向于已有流动性的检测```</br>
```
# `手动设置`参数&判断条件（根据补充叙述中的`1`,`2`参数设置与条件判断会略有差异）
```
交易路由及链的选择（例如：Uniswap & Pancakeswap)（`1`,`2`均适用）</br>
目标币合约地址(选择抢跑/夹取的目标对象）（`1`,`2`均适用）</br>
目标合约地址风险监测</br>
GAS费设置（对于执行抢跑/夹取行为的Gas费设置）</br>
用户登陆（参与抢跑/夹取行为的钱包登陆-支持Web钱包的直连与扫码登陆）</br>
机器人需计算每笔交易是否能够盈利，若无法盈利则不执行该笔交易，可盈利则反之，交易策略及速度须胜过多数夹子机器人</br>
```
