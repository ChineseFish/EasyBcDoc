# 交易共识

UNL中的Server节点对合并之后的cadidate set中的交易进行投票。获得“赞成”票数超过最低百分比的交易，如果有，将传递到下一轮，而未获得足够票数的交易将被放弃，或列入下一个Open Ledger的candidate set。最后一轮同步过程要求candidate set中的交易至少获取80%的Server节点的确认。剩余下来的所有的交易会被用于下一个Open Ledger，当前的Open Ledger随后会被关闭，从而转变为Last-Closed Ledger。