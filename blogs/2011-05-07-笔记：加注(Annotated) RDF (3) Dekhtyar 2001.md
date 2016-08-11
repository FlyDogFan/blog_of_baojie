笔记：加注(Annotated) RDF (3) Dekhtyar 2001
---
    
> Categories: 笔记, 语义网, 逻辑  
> Time: 2011-05-07
    
Alex Dekhtyar, Robert B. Ross, V. S. Subrahmanian: Probabilistic temporal databases, I: algebra. ACM Trans. Database Syst. 26(1): 41-95 (2001)正文44页，共67页。背景：这个似乎和Annotated RDF无关。不过，temporal information是一种最常见的annotation，而在tuple上的工作，自然也可以用在triple上。Alexander Dekhtyar是Subrahmanian 2000年毕业的PhD。后面的APT (Annotated Probabilistic Temporal) Logic [Shakarian 2011]看似是这个工作的扩展基本建模对象：Data tuple d is in relation R at some point of time in the interval [ti, tj ] with probability between p1 and p2. 例：Package p will arrive in Albany at some time between 9am and 5pm on Nov. 8 with probability 50–60%Rain is expected to begin sometime between 2pm and 12 midnight on Nov. 8 with probability 5–20%IBM stockwill reach $300 per share some time during the time interval Nov 1-10 with probability 90-100%时间的模型：文中Fig 1 普通数据库，时态数据库和概率时态数据库的区别Time Unit: 比如天 day={1,2,…,31}Linear hierarchy of time units: 比如 day < month < yearTime point: 是一个tuple，每个分量来自hierarchy中的一层，例如(2011 May 7 Sat 18 28)Calendar: 规定了time point的合法性，比如(2011 Feb 31)是不合法的Temporal constraint: 基本的约束是形如day >= 5 或者 (2011 May 1 ~ 2011 May 7) 【注，原文要求(t1 ~ t2)里t1晚于t2，反直觉】。复杂的约束由基本约束通过 与∧ 或∨ 非¬ 构造。例 (year=1996 ∧ month < 4)【待续】     
    