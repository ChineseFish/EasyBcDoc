# 交易校验

UNL中服务器对合并之后的cadidate set中的交易进行投票。获得“赞成”票数的最低百分比以上的交易，如果有，将传递到下一轮，而未获得足够票数的交易将被放弃，或列入下一个Open Ledger的candidate set。最后一轮一致性过程要求candidate set中的交易至少获取80%的服务器的确认。剩余下来的所有的交易会被用于Open Ledger，这个Open Ledger随后会被关闭，从而转变为Last-closed Ledger。