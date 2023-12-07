# CBSH2代码记录

## 相关细节

### 下标含义

* `typedef std::tuple<int, int, int, int, int> Conflict;`
  * vertex: agent1, agent2, loc, -1, time
  * edge: agent1, agent2, loc1, loc2, time
  * rec: agent1, agent2, Rg(负数), time1, time2
  
* `typedef std::tuple<int, int, int> Constraint;`
  * vertex: loc, -1, time
  * edge : loc1, loc2, time
  * rec: loc1(负数), loc2, time (loc1 - loc2都增加点约束)

### 结构体、变量

* `generateChild----lowerbound`
  * 作为单agent寻路的参数

### 函数

## 待解决问题

* Rectangle Conflict处理时不用考虑区间所在的时间点吗	
  * 首先保证了是有冲突的。即是否 有冲突 + 有Rec -》 有Rec冲突
  * 没有Rec冲突-》时间点不会对上？

* 为什么要在High Level一个节点搜索完后releaseMDD（删除对应agent的MDD中层数最少的）
  * MDD占内存较多，有数量上限，优先删除可能后续没用的

* path length constrain，这里的BC用长度限制吗？
  * 用处不大

