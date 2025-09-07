# sofa-jraft 快速上手

实现一个简单的分布式 Counter 服务

用户需要实现的部分：
1. Request、 Response 请求和返回对象定义
   - Request: 定义请求对象
   - Response: 定义返回对象
   - 都需要实现 Serializable 接口
2. Processor 处理用户请求（业务逻辑）
    - 实现 handleRequest 方法: 处理请求
3. StateMachine 状态机实现（持久化和状态机应用）
   - onApply 方法: 执行 task，更新状态机
   - onSnapshotSave 方法: 保存快照
   - onSnapshotLoad 方法: 加载快照

Sofa-JRaft 保证多节点的状态一致性
