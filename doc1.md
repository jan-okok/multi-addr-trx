### 出账/推确认数回调接口

| 字段 | 类型 | 是否必须 | 说明 |
| -------- | -------- | -------- |
| apinonce     | string    | Y   |API 随机数     |
| apisign     | string    | Y   |API 签名     |
| apits     | int    | Y   |API 时间戳     |
| client_id     | string    | Y   |商户id     |
| outer_order_no     | string      | N    |交易所订单编号，仅出账交易有值 （注意：旧的字段outOrderId废弃不再使用）    |
| block_height     | int      | Y     |区块高度 |
| amount     | string      | Y     |订单金额/入账金额     |
| coin     | string    | Y   |链    |
| coin_type     | string    | Y   |币种类型    |
| confirm_time     | int    | Y   |确认时间     |
| confirmations     | int    | Y   |确认数     |
| contract_address     | string    | Y   |合约地址 （注意：旧的字段contractAddress废弃不再使用）     |
| fee     | string    | Y   |手续费     |
| from_address     | string    | Y   |交易转账人地址     |
| to_address     | string    | Y   |交易接收人地址     |
| from_trx_id     | string    | N  | 暂不清楚     |
| to_raw_address     | string    | N  | 暂不清楚     |
| is_in     | int    | Y  | 是否入账；1：入账，2：出账     |
| memo     | string    | N  | 交易附带的memo     |
| timestamp     | int    | Y  | 此交易数据生成的时间     |
| transaction_id     | string    | Y  | 交易哈希（注意：旧的字段txid废弃不再使用）     |
| trx_n     | int    | Y  | 交易下标，从0开始    |
| user_sub_id     | int    | Y  | 对应钱包商户id    |
| order_split_tx_count    | int    | Y  | 订单拆分交易数量 **(多地址出账版本新增)**   |
| txs    | List    | Y  | 交易列表**(多地址出账版本新增)** |
| &nbsp;&nbsp;&nbsp;seq_no     | string      | Y     |交易流水号 |
| &nbsp;&nbsp;&nbsp;status     | int      | Y     |交易状态；1：正常，2：失败交易 |
| &nbsp;&nbsp;&nbsp;block_height     | int      | Y     |区块高度 |
| &nbsp;&nbsp;&nbsp;amount     | string      | Y     |订单金额/入账金额     |
| &nbsp;&nbsp;&nbsp;confirm_time     | int    | Y   |确认时间     |
| &nbsp;&nbsp;&nbsp;confirmations     | int    | Y   |确认数     |
| &nbsp;&nbsp;&nbsp;fee     | string    | Y   |手续费     |
| &nbsp;&nbsp;&nbsp;from_address     | string    | Y   |交易转账人地址     |
| &nbsp;&nbsp;&nbsp;to_address     | string    | Y   |交易接收人地址     |
| &nbsp;&nbsp;&nbsp;memo     | string    | N  | 交易附带的memo     |
| &nbsp;&nbsp;&nbsp;timestamp     | int    | Y  | 此交易数据生成的时间     |
| &nbsp;&nbsp;&nbsp;transaction_id     | string    | Y  | 交易哈希（注意：旧的字段txid废弃不再使用）     |
| &nbsp;&nbsp;&nbsp;trx_n     | int    | Y  | 交易下标，从0开始    |

### 说明
txs.status：当前此值为2表示失败的交易；交易所也需要把此交易设置为失败。
