#### 1.建立passing network

无向带权图（根据题目中的要求，微观时间中建立一分钟内的传球情况图，宏观时间建立整场游戏的图，我理解中是两幅图，结果是win的一场比赛、结果是lose的一场比赛）

- network属性（一些可用的指标）：

  - k-核数：

    > 一个图的k-核是指反复去掉度小于或等于k的节点所剩余的子图。存在于k-核的节点，在（k+1）-核中被除去，则k就是该节点的核数。

    可用于度量节点在图中的深度，图的核数大，说明整个网络具有的层次较深。本题中体现为整个团队的合作程度高。

  - 平均权重：边的权重总值除以节点总数

  - 各节点度数的方差【3】

  - average shortest path d【2】：（计算量略大）

    任意两名队员之间最短路径的平均值。反映connected程度。

    ……

  可以根据以上各种指标来综合建立反映团队协作程度的量化指标

  短时间内的传球模式

- 探索多重尺度

  时间的宏观角度通过一场比赛的网图可以做出分析，微观角度可以做如下方面的展示：

  1）网络节点中心（度数最大的节点）每分钟的移动情况

  2）（具体参见第二个reference第6页）

  队员微观角度？（题目中的叙述是两两之间）

#### 2. 数据分析

结合上一个流程中的传球网络中的节点的度数、题目数据中提取的每一个队员的进球数、犯规罚球等其他因素，对队员的行为进行量化指标评定，作出队伍结构配置。

如何确定team level process指标？如何捕获团队合作的动态方面？

#### 3.一些问题

题目中的在团队运动的受控环境中考虑群体动力学怎么实现？

#### 4. workflow

evaluation: 通过网络确定指标

modeling: 通过指标等分析团队结构配置动态

playerrank

strategy-making: 结合上述作出决策

