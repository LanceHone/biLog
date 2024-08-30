# biLog
separate the bussiness log and system log.

目标: 通过注解记录业务日志  

e.g. ```@LogRecord(content = "修改了订单的配送员：从“{queryOldUser{#request.deliveryOrderNo()}}”, 修改到“{deveryUser{#request.userId}}”",bizNo="#request.deliveryOrderNo")``` 

由于日至普遍包含以下元素： 操作人 被操作的业务对象  原数据 -> 新数据  

客户端通过实现`OperatorGetService`、`ILogRecordService`、`IParseFunction` 自定义操作人，日志记录方法（入库和查询等），和自定义处理函数


