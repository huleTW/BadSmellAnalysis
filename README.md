# bad-smell-analysis

## graph-call - 连通图式引用问题的识别
* 调用定义：连通图式引用表现为多个类之间存在引用关系，比如A->B->C,同时A->C,这意味着，代码在初时没有经过良好的抽象组织。
* 副作用：
    * 随着参与类或方法数量的增加，引用关系会越来越复杂。容易产生数据泥团
    * 当需求增加时，由于抽象层次混乱，类之间的职责不清，导致代码逻辑混乱
* 解决该问题后带来的收益
    * 代码逻辑的内聚
    * 提高可读性和组织性
    * 便于后续维护