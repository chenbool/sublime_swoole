# sublime_swoole

Sublime Text 的 Swoole 代码片段插件，提供 Swoole 常用类和方法的自定义代码片段。

> 当前版本基于 Swoole 4.6+ 官方文档编写

## 安装

### Sublime Text 安装

1. 打开 Sublime Text
2. 按 `Ctrl+Shift+P` 打开命令面板
3. 输入 `Package Control: Install Package`
4. 搜索 `swoole` 并安装

### 手动安装

将项目克隆到 Sublime Text 的 Packages 目录：

```bash
git clone https://github.com/chenbool/sublime_swoole.git
```

Windows 用户将文件复制到：
- Sublime Text 3: `%APPDATA%\Sublime Text 3\Packages\`
- Sublime Text 4: `%APPDATA%\Sublime Text 4\Packages\`

Linux 用户：
- `~/.config/sublime-text-3/Packages/` 或 `~/.config/sublime-text/Packages/`

Mac 用户：
- `~/Library/Application Support/Sublime Text 3/Packages/` 或 `~/Library/Application Support/Sublime Text/Packages/`

## 使用方法

在 Sublime Text 中输入对应的触发词，按 `Tab` 键即可自动补全。

## Swoole 类和方法列表

### Swoole\Server

| 触发词 | 说明 |
|--------|------|
| swoole_server | Swoole\Server 构造函数 |
| swoole_server_construct | Swoole\Server 构造函数 |
| swoole_server_set | 设置服务器配置 |
| swoole_server_on | 注册事件回调 |
| swoole_server_start | 启动服务器 |
| swoole_server_stop | 停止服务器 |
| swoole_server_shutdown | 关闭服务器 |
| swoole_server_reload | 重载配置 |
| swoole_server_send | 发送数据 |
| swoole_server_sendto | UDP发送数据 |
| swoole_server_sendwait | 阻塞发送 |
| swoole_server_sendfile | 发送文件 |
| swoole_server_sendMessage | 发送消息到工作进程 |
| swoole_server_close | 关闭连接 |
| swoole_server_connection_info | 获取连接信息 |
| swoole_server_connection_list | 获取连接列表 |
| swoole_server_getClientInfo | 获取客户端详细信息 |
| swoole_server_getClientList | 获取客户端列表 |
| swoole_server_task | 投递异步任务 |
| swoole_server_taskwait | 等待任务完成 |
| swoole_server_taskWaitMulti | 批量等待任务 |
| swoole_server_finish | 任务完成回调 |
| swoole_server_after | 延时执行 |
| swoole_server_tick | 定时器 |
| swoole_server_clearTimer | 清除定时器 |
| swoole_server_defer | 延迟执行 |
| swoole_server_stats | 获取服务器状态 |
| swoole_server_bind | 绑定uid |
| swoole_server_protect | 保护连接 |
| swoole_server_addlistener | 添加监听 |
| swoole_server_addProcess | 添加自定义进程 |
| swoole_server_listen | 监听端口 |
| swoole_server_pause | 暂停接收 |
| swoole_server_resume | 恢复接收 |
| swoole_server_confirm | 确认连接 |
| swoole_server_exist | 检查连接是否存在 |
| swoole_server_heartbeat | 心跳检测 |
| swoole_server_getLastError | 获取最后错误码 |

### Swoole\Http\Server

| 触发词 | 说明 |
|--------|------|
| swoole_http_server | Swoole\Http\Server 构造函数 |
| swoole_http_server_start | 启动HTTP服务器 |
| swoole_http_server_on | 注册HTTP事件 |

### Swoole\Http\Request

| 触发词 | 说明 |
|--------|------|
| swoole_http_request_rawcontent | 获取原始内容 |
| swoole_http_request_destruct | 销毁请求 |
| swoole_http_request_create | 创建请求对象 (4.6+) |
| swoole_http_request_parse | 解析请求 (4.6+) |
| swoole_http_request_isCompleted | 检查请求是否完成 (4.6+) |
| swoole_http_request_getMethod | 获取请求方法 (4.6+) |

### Swoole\Http\Response

| 触发词 | 说明 |
|--------|------|
| swoole_http_response_end | 结束响应 |
| swoole_http_response_header | 设置响应头 |
| swoole_http_response_status | 设置HTTP状态 |
| swoole_http_response_cookie | 设置Cookie |
| swoole_http_response_rawcookie | 设置原始Cookie |
| swoole_http_response_gzip | 启用Gzip压缩 |
| swoole_http_response_sendfile | 发送文件 |
| swoole_http_response_write | 写入响应体 |
| swoole_http_response_initHeader | 初始化响应头 |

### Swoole\Client (同步)

| 触发词 | 说明 |
|--------|------|
| swoole_client | Swoole\Client 构造函数 |
| swoole_client_connect | 连接服务器 |
| swoole_client_send | 发送数据 |
| swoole_client_sendto | UDP发送 |
| swoole_client_sendfile | 发送文件 |
| swoole_client_recv | 接收数据 |
| swoole_client_close | 关闭连接 |
| swoole_client_isConnected | 检查连接状态 |
| swoole_client_getpeername | 获取对端地址 |
| swoole_client_getsockname | 获取本地地址 |
| swoole_client_set | 设置参数 |
| swoole_client_on | 注册回调 |
| swoole_client_pause | 暂停接收 |
| swoole_client_resume | 恢复接收 |
| swoole_client_pipe | 管道通信 |
| swoole_client_sleep | 休眠 |
| swoole_client_wakeup | 唤醒 |

### Swoole\Process

| 触发词 | 说明 |
|--------|------|
| swoole_process | Swoole\Process 构造函数 |
| swoole_process_construct | 构造函数 |
| swoole_process_start | 启动进程 |
| swoole_process_write | 写入管道 |
| swoole_process_read | 读取管道 |
| swoole_process_close | 关闭管道 |
| swoole_process_push | 消息队列推送 |
| swoole_process_pop | 消息队列弹出 |
| swoole_process_kill | 终止进程 |
| swoole_process_signal | 信号处理 |
| swoole_process_alarm | 定时信号 |
| swoole_process_wait | 等待子进程 |
| swoole_process_exec | 执行外部命令 |
| swoole_process_daemon | 守护进程化 |
| swoole_process_name | 设置进程名 |
| swoole_process_exit | 退出进程 |
| swoole_process_useQueue | 启用消息队列 |
| swoole_process_statQueue | 获取队列状态 |
| swoole_process_freeQueue | 释放队列 |

### Swoole\Table

| 触发词 | 说明 |
|--------|------|
| swoole_table | Swoole\Table 构造函数 |
| swoole_table_construct | 构造函数 |
| swoole_table_column | 定义列 |
| swoole_table_create | 创建表 |
| swoole_table_set | 设置行 |
| swoole_table_get | 获取行 |
| swoole_table_del | 删除行 |
| swoole_table_exists | 检查行是否存在 |
| swoole_table_inc | 原子自增 |
| swoole_table_decr | 原子自减 |
| swoole_table_count | 获取行数 |
| swoole_table_foreach | 遍历表 |
| swoole_table_current | 当前行 |
| swoole_table_key | 当前键 |
| swoole_table_next | 下一行 |
| swoole_table_rewind | 重置指针 |
| swoole_table_valid | 检查有效性 |
| swoole_table_destroy | 销毁表 |

### Swoole\Timer

| 触发词 | 说明 |
|--------|------|
| swoole_timer_tick | 定时器 |
| swoole_timer_after | 延时执行 |
| swoole_timer_clear | 清除定时器 |
| swoole_timer_exists | 检查定时器 |

### Swoole\Lock

| 触发词 | 说明 |
|--------|------|
| swoole_lock | Swoole\Lock 构造函数 |
| swoole_lock_construct | 构造函数 |
| swoole_lock_lock | 加锁 |
| swoole_lock_lock_read | 读锁 |
| swoole_lock_trylock | 尝试加锁 |
| swoole_lock_trylock_read | 尝试读锁 |
| swoole_lock_unlock | 解锁 |
| swoole_lock_destruct | 销毁锁 |

### Swoole\Buffer

| 触发词 | 说明 |
|--------|------|
| swoole_buffer | Swoole\Buffer 构造函数 |
| swoole_buffer_construct | 构造函数 |
| swoole_buffer_append | 追加数据 |
| swoole_buffer_write | 写入数据 |
| swoole_buffer_read | 读取数据 |
| swoole_buffer_substr | 截取子串 |
| swoole_buffer_expand | 扩展空间 |
| swoole_buffer_recycle | 回收空间 |
| swoole_buffer_clear | 清空缓冲区 |
| swoole_buffer_tostring | 转换为字符串 |
| swoole_buffer_destruct | 销毁缓冲区 |

### Swoole\Channel

| 触发词 | 说明 |
|--------|------|
| swoole_channel | Swoole\Channel 构造函数 |
| swoole_channel_construct | 构造函数 |
| swoole_channel_push | 推送数据 |
| swoole_channel_pop | 弹出数据 |
| swoole_channel_stats | 获取状态 |
| swoole_channel_destruct | 销毁通道 |

### Swoole\Atomic

| 触发词 | 说明 |
|--------|------|
| swoole_atomic | Swoole\Atomic 构造函数 |
| swoole_atomic_construct | 构造函数 |
| swoole_atomic_add | 加法 |
| swoole_atomic_sub | 减法 |
| swoole_atomic_get | 获取值 |
| swoole_atomic_set | 设置值 |
| swoole_atomic_cmpset | 比较并设置 |

### Swoole\Event

| 触发词 | 说明 |
|--------|------|
| swoole_event_add | 添加事件 |
| swoole_event_del | 删除事件 |
| swoole_event_set | 设置事件 |
| swoole_event_write | 写事件 |
| swoole_event_defer | 延迟执行 |
| swoole_event_exit | 退出事件循环 |
| swoole_event_wait | 等待事件 |

### Swoole 异步函数

| 触发词 | 说明 |
|--------|------|
| swoole_async_read | 异步读文件 |
| swoole_async_write | 异步写文件 |
| swoole_async_readfile | 异步读文件内容 |
| swoole_async_writefile | 异步写文件内容 |
| swoole_async_dns_lookup | 异步DNS查询 |
| swoole_async_set | 异步参数设置 |

### Swoole\Coroutine 全局函数

| 触发词 | 说明 |
|--------|------|
| swoole_coroutine_create | 创建协程 (go) |
| swoole_coroutine_resume | 恢复协程 |
| swoole_coroutine_suspend | 挂起协程 |
| swoole_coroutine_getuid | 获取协程ID |
| swoole_coroutine_cli_wait | 等待CLI |
| swoole_coroutine_call_user_func | 调用函数 |
| swoole_coroutine_call_user_func_array | 数组调用 |
| swoole_coroutine_run | 运行协程 (run) |
| swoole_coroutine_sleep | 协程睡眠 |
| swoole_coroutine_getuid | 获取UID |

### Swoole\Coroutine\Client

| 触发词 | 说明 |
|--------|------|
| swoole_coroutine_client | 协程客户端 |
| swoole_coroutine_client_construct | 构造函数 |
| swoole_coroutine_client_connect | 连接 |
| swoole_coroutine_client_send | 发送 |
| swoole_coroutine_client_recv | 接收 |
| swoole_coroutine_client_close | 关闭 |
| swoole_coroutine_client_sendto | UDP发送 |
| swoole_coroutine_client_sendfile | 发送文件 |
| swoole_coroutine_client_getpeername | 获取地址 |
| swoole_coroutine_client_getsockname | 获取本地地址 |
| swoole_coroutine_client_isConnected | 检查连接 |
| swoole_coroutine_client_set | 设置参数 |
| swoole_coroutine_client_destruct | 销毁 |

### Swoole\Coroutine\Http\Client

| 触发词 | 说明 |
|--------|------|
| swoole_coroutine_http_client | HTTP客户端 |
| swoole_coroutine_http_client_construct | 构造函数 |
| swoole_coroutine_http_client_get | GET请求 |
| swoole_coroutine_http_client_post | POST请求 |
| swoole_coroutine_http_client_execute | 执行请求 |
| swoole_coroutine_http_client_set | 设置参数 |
| swoole_coroutine_http_client_setHeaders | 设置头 |
| swoole_coroutine_http_client_setCookies | 设置Cookie |
| swoole_coroutine_http_client_setData | 设置数据 |
| swoole_coroutine_http_client_setMethod | 设置方法 |
| swoole_coroutine_http_client_setDefer | 设置延迟 |
| swoole_coroutine_http_client_getDefer | 获取延迟状态 |
| swoole_coroutine_http_client_addFile | 添加文件 |
| swoole_coroutine_http_client_isConnected | 检查连接 |
| swoole_coroutine_http_client_close | 关闭 |
| swoole_coroutine_http_client_destruct | 销毁 |

### Swoole\Coroutine\MySQL

| 触发词 | 说明 |
|--------|------|
| swoole_coroutine_mysql | MySQL客户端 |
| swoole_coroutine_mysql_construct | 构造函数 |
| swoole_coroutine_mysql_connect | 连接 |
| swoole_coroutine_mysql_query | 查询 |
| swoole_coroutine_mysql_recv | 接收结果 |
| swoole_coroutine_mysql_close | 关闭 |
| swoole_coroutine_mysql_destruct | 销毁 |

### Swoole\Coroutine\Redis

| 触发词 | 说明 |
|--------|------|
| swoole_coroutine_redis | Redis客户端 |
| swoole_coroutine_redis_connect | 连接 |

### Swoole\Coroutine\Socket

| 触发词 | 说明 |
|--------|------|
| swoole_coroutine_socket | 协程Socket |
| swoole_coroutine_socket_connect | 连接 |
| swoole_coroutine_socket_send | 发送 |
| swoole_coroutine_socket_recv | 接收 |
| swoole_coroutine_socket_close | 关闭 |

### Swoole\WebSocket\Server

| 触发词 | 说明 |
|--------|------|
| swoole_websocket_server | WebSocket服务器 |
| swoole_websocket_server_construct | 构造函数 |
| swoole_websocket_server_push | 推送消息 |
| swoole_websocket_server_pack | 打包数据 |
| swoole_websocket_server_unpack | 解包数据 |
| swoole_websocket_server_on | 注册回调 |
| swoole_websocket_server_exist | 检查连接 |

### Swoole\Redis\Server

| 触发词 | 说明 |
|--------|------|
| swoole_redis_server | Redis服务器 |
| swoole_redis_server_start | 启动 |
| swoole_redis_server_setHandler | 设置处理器 |
| swoole_redis_server_format | 格式化响应 |

### Swoole\Serialize

| 触发词 | 说明 |
|--------|------|
| swoole_serialize_pack | 序列化 |
| swoole_serialize_unpack | 反序列化 |

### Swoole\MMap

| 触发词 | 说明 |
|--------|------|
| swoole_mmap_open | 内存映射 |

### Swoole\Connection\Iterator

| 触发词 | 说明 |
|--------|------|
| swoole_connection_iterator_count | 连接数量 |
| swoole_connection_iterator_current | 当前连接 |
| swoole_connection_iterator_key | 连接键 |
| swoole_connection_iterator_next | 下一个 |
| swoole_connection_iterator_offsetExists | 偏移是否存在 |
| swoole_connection_iterator_offsetGet | 获取偏移 |
| swoole_connection_iterator_offsetSet | 设置偏移 |
| swoole_connection_iterator_offsetUnset | 取消设置 |
| swoole_connection_iterator_rewind | 重置 |
| swoole_connection_iterator_valid | 是否有效 |

### Swoole Server 端口

| 触发词 | 说明 |
|--------|------|
| swoole_server_port | 服务器端口 |
| swoole_server_port_construct | 构造函数 |
| swoole_server_port_on | 注册回调 |
| swoole_server_port_set | 设置参数 |
| swoole_server_port_destruct | 销毁 |

### Swoole 常量

| 触发词 | 说明 |
|--------|------|
| SWOOLE_BASE | BASE模式 |
| SWOOLE_PROCESS | PROCESS模式 |
| SWOOLE_ASYNC | 异步模式 |
| SWOOLE_SYNC | 同步模式 |
| SWOOLE_TCP | TCP |
| SWOOLE_UDP | UDP |
| SWOOLE_TCP6 | TCP IPv6 |
| SWOOLE_UDP6 | UDP IPv6 |
| SWOOLE_SOCK_TCP | TCP套接字 |
| SWOOLE_SOCK_UDP | UDP套接字 |
| SWOOLE_SOCK_TCP6 | TCP IPv6 |
| SWOOLE_SOCK_UDP6 | UDP IPv6 |
| SWOOLE_SOCK_UNIX_STREAM | Unix域流 |
| SWOOLE_SOCK_UNIX_DGRAM | Unix域数据报 |
| SWOOLE_MUTEX | 互斥锁 |
| SWOOLE_SEM | 信号量 |
| SWOOLE_RWLOCK | 读写锁 |
| SWOOLE_FILELOCK | 文件锁 |
| SWOOLE_IPC_MSGQUEUE | 消息队列 |
| SWOOLE_IPC_PREEMPTIVE | 抢占式IPC |
| SWOOLE_IPC_UNSOCK | Unix套接字 |
| SWOOLE_KEEP | KeepAlive |
| SWOOLE_FAST_PACK | 快速打包 |
| SWOOLE_EVENT_READ | 读事件 |
| SWOOLE_EVENT_WRITE | 写事件 |
| SWOOLE_EVENT_LOOP | 循环事件 |
| SWOOLE_THREAD | 线程模式 |
| SWOOLE_AIO_BASE | 基础异步IO |
| SWOOLE_AIO_LINUX | Linux异步IO |
| WEBSOCKET_OPCODE_TEXT | 文本帧 |
| WEBSOCKET_OPCODE_BINARY | 二进制帧 |
| WEBSOCKET_OPCODE_PING | Ping帧 |
| WEBSOCKET_STATUS_CONNECTION | 连接状态 |
| WEBSOCKET_STATUS_HANDSHAKE | 握手状态 |
| WEBSOCKET_STATUS_FRAME | 帧状态 |
| WEBSOCKET_STATUS_ACTIVE | 活跃状态 |
| SWOOLE_VERSION | 版本号 |

## Swoole 函数列表

### 全局函数

| 触发词 | 说明 |
|--------|------|
| swoole_version | 获取Swoole版本 |
| swoole_cpu_num | CPU核心数 |
| swoole_last_error | 最后错误 |
| swoole_errno | 错误码 |
| swoole_strerror | 错误信息 |
| swoole_get_local_ip | 获取本地IP |
| swoole_client_select | 客户端选择 |
| swoole_select | 选择 |
| swoole_load_module | 加载模块 |

## 相关链接

- [Sublime Text 官方](https://www.sublimetext.com/)
- [Swoole 官方文档](https://www.swoole.com/)
- [Swoole 源码](https://github.com/swoole/swoole-src)
- [OpenSwoole API](https://openswoole.com/swoole-api)

## 其他插件

- [sublime_yaf](https://github.com/bool1993/sublime_yaf) - Yaf 代码片段
- [sublime_thinkphp5](https://github.com/bool1993/sublime_thinkphp5) - ThinkPHP5 代码片段
