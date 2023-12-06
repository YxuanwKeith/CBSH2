# CBSH2代码记录

## 相关细节

### 下标含义

* `typedef std::tuple<int, int, int, int, int> Conflict;`
  * vertex: agent1, agent2, loc, -1, time
  * edge: agent1, agent2, loc1, loc2, time
  * rec: agent1, agent2, Rg, time1, time2
  
* `typedef std::tuple<int, int, int> Constraint;`
  * vertex: loc, -1, time
  * edge : loc1, loc2, time
  * rec: 

### 结构体、变量

* `generateChild----lowerbound`

### 函数

* `addModifiedBarrierConstraints`

rectangle constrain 不用考虑时间？