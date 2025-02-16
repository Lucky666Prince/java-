# 关于Slot的理解

1.参数值的存放总是在局部变量数组的index0开始,到数组长度-1的索引结束。

2.局部变量表，最基本的存储单元是slot（变量槽）局部变量表中存放编译期可知的各种基本数据类型（8种），引用类型(reference), returnAddress类型的变量。

3.在局部变量表里, 32位以内的类型只占用一个slot (包括returnAddress类型），64位的类型（long和double）占用两个slot.

byte、short、char 在存储前被转换为int， boolean 也被转换为int，0 表示false ， 非0 表示true。

long和double则占据两个slot.

