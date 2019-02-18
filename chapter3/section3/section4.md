# 一致性
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>
为了满足一致性要求，必须表明所有nonfaulty节点（不管它们的UNLS）在相同的一组交易上达成了共识。因为每个服务器的UNLS可以是不同的，所以一致性无法通过正确性证明来进行保证。例如，如果对UNL的成员资格没有任何限制，并且UNL的大小不大于\\(0.2 * n_{total}\\)，其中\\(n_{total}\\)整个分布式交易系统中节点的数量，那么就有可能有一个分叉。这可以用一个简单的例子来说明，如下图：
![younghz的Markdown库](/asserts/2.bmp "图二")
####图2.防止两个UNL集团之间出现分叉所需的连接性示例。
想象UNL图中的两个小圈子，每一个都大于\\(0.2 * n_{total}\\)。所谓小圈子，我们指的是一组节点，其中每个节点的UNL是完全相同的一组节点。因为这两个小圈子不共享任何成员，所以每个小圈子都有可能实现一个正确的一致性过程。如果两个小圈子的连通性超过\\(0.2 * n_{total}\\)，那么分叉就不再可能了，因为两个小圈子之间存在分歧会阻止整个系统在80%一致性阈值上达成共识。
下面是达成共识所需要的最小连通率的共识：
$$|UNL_i \cap UNL_j| \geq \frac{1}{5}max(|UNL_i|, |UNL_j|) \forall i,j$$
