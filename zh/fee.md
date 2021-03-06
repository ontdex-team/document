# Ontdex手续费说明

ontdex是ontology上的第一个去中心化交易所，支持ONT与ONG两大原生token之间的交易，支持以ONG为报价货币的OEP-4 token，OEP-5 token，OEP-8 token的交易对。
如果ontology上会有符合OEP4标准的稳定币，ontdex也会支持以稳定币作为报价货币的交易对。

鉴于去中心化交易所的特殊性以及ONT的精度问题，ontdex对于每个交易对将统一使用报价货币作为手续费，具体规则和手续费费率如下：

1. ontdex当前手续费费率为千分之二，买卖双方均需支付；

2. 交易成功的卖方需支付交易总额的千分之二作为手续费，例如：ONT/ONG交易对，以1.0的价格卖出了10个ONT，则交易总额为10ONG，这时需支付0.02的手续费，所以实际
买入的ONG数量为9.98；

3. 交易的买方需支付交易总额的千分之二作为手续费，这部分手续费将提前转入ontdex智能合约，并且在成交的时候支付；如果用户撤单，手续费也将一起退回；
例如：ONT/ONG交易对，用户下了一个价格为1.0，数量为10ONT的单，则交易总额为10ONG，用户下单的时候将向合约转入10个ONG用于交易，同时也将转入0.02个ONG作为预付
的手续费，当订单成交了5个ONT时，用户将收到5个ONT，并且预付的手续费将扣除0.01ONG，这时用户撤单，则用户的账户将收到剩余的未交易的5个ONG以及未消耗的0.01个
ONG。

4. 下单限制：由于链上手续费的缘故，ontdex对每一笔挂单都进行了最小交易额的限制，当下单金额小于该值时，用户将无法下单成功，当前最小交易额限制为10ONG。
