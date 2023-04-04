# sys23
投研平台（自用）

自用的回测框架，只限个人使用。

- ***目录[`api`](api): 接口***
- [`load_tushare`](api/load_tushare.py): 从[Tushare](https://tushare.pro/)获取基础数据
- [`combine_tushare`](api/combine_tushare.py): 将日度流量数据整合成面板数据
- 
- ***目录[`data`](data): 数据相关***
- 
- ***目录[`demo`](demo): 功能/策略的展示***
- [`mkt_dvg_min_amt`](demo/mkt_dvg_min_amt.ipynb): 成交额市场分歧度择时【因子】
- 
- ***目录[`idea`](idea): 想法***
- 


---

## [本地数据](./cache)

| 名称                                                         | 类型                | 描述                                                         |
| :----------------------------------------------------------- | :------------------ | :----------------------------------------------------------- |
| [tradedates.csv](tradedates.csv)                             | str                 | 交易日期                                                     |
| [daily](https://tushare.pro/document/2?doc_id=27) + [adj_factor](https://tushare.pro/document/2?doc_id=28) | 日线行情 + 复权因子 | 【交易日每天15点～16点之间入库】【复权因子更新时间：早上9点30分】 |
| [openAdj.csv](cache/openAdj.csv)                             | float               | 开盘价 x 复权因子                                            |
| [highAdj.csv](cache/highAdj.csv)                             | float               | 最高价 x 复权因子                                            |
| [lowAdj.csv](cache/lowAdj.csv)                               | float               | 最低价 x 复权因子                                            |
| [closeAdj.csv](cache/closeAdj.csv)                           | float               | 收盘价 x 复权因子                                            |
| [vol.csv](cache/vol.csv)                                     | float               | 成交量 （手）                                                |
| [amount.csv](cache/amount.csv)                               | float               | 成交额 （千元）                                              |
| [daily_basic](https://tushare.pro/document/2?doc_id=32)      | 每日指标            | 获取全部股票每日重要的基本面指标，可用于选股分析、报表展示等。【更新时间：交易日每日15点～17点之间】 |
| turnover_rate                                                | float               | 换手率（%）                                                  |
| turnover_rate_f                                              | float               | 换手率（自由流通股）                                         |
| volume_ratio                                                 | float               | 量比                                                         |
| pe                                                           | float               | 市盈率（总市值/净利润， 亏损的PE为空）                       |
| pe_ttm                                                       | float               | 市盈率（TTM，亏损的PE为空）                                  |
| pb                                                           | float               | 市净率（总市值/净资产）                                      |
| ps                                                           | float               | 市销率                                                       |
| ps_ttm                                                       | float               | 市销率（TTM）                                                |
| dv_ratio                                                     | float               | 股息率 （%）                                                 |
| dv_ttm                                                       | float               | 股息率（TTM）（%）                                           |
| total_share                                                  | float               | 总股本 （万股）                                              |
| float_share                                                  | float               | 流通股本 （万股）                                            |
| free_share                                                   | float               | 自由流通股本 （万）                                          |
| total_mv                                                     | float               | 总市值 （万元）                                              |
| circ_mv                                                      | float               | 流通市值（万元）                                             |
| [idx_weight](cache/index_weight/README.md)                   | 指数成分和权重      | 获取各类指数成分和权重，**月度数据** 。来源：指数公司网站公开数据 |
| [index_weight_CSI300.csv](cache/index_weight_CSI300.csv)     | float               |                                                              |
| [index_weight_CSI500.csv](cache/index_weight_CSI500.csv)     | float               |                                                              |
| [index_weight_CSI800.csv](cache/index_weight_CSI800.csv)     | float               |                                                              |
| [index_weight_CSI1000.csv](cache/index_weight_CSI1000.csv)   | float               |                                                              |
