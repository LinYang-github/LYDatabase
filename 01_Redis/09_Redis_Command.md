# 命令

PING   
该命令用于检测redis服务是否启动

-h host -p port -a password   
e.g. -h 127.0.0.1 -p 6379 -a "mypass"   
需要在远程redis服务上执行命令

##

### Redis键(key) ###
COMMAND KEY_NAME    

SET mykey redis   
DEL mykey   在key存在时删除key   
DUMP mykey   序列化给定key，并返回被序列化的值   
EXISTS mykey   检查给定key是否存在   
EXPIRE mykey seconds   为给定key设置过期时间   
EXPIREAT mykey timestamp   都用于为mykey设置过期时间。不同在于EXPIREAT命令接受的时间参数是UNIX时间戳   
PEXPIRE mykey milliseconds   设置mykey的过期时间亿以毫秒计   
PEXPIREAT mykey milliseconds-timestamp   设置mykey过期时间的时间戳(unix timestamp)以毫秒计   
KEYS pattern   查找所有符合给定模式(pattern)的key   
MOVE key db   将当前数据库的key移动到给定的数据库db当中   
PERSIST key   移除key的过期时间，key将持久保持   
PTTL key   以毫秒为单位返回key的剩余的过期时间   
TTL key   以秒为单位，返回给定key的剩余生存时间   
RANDOMKEY   从当前数据库中随机返回一个key   
RENAME key newkey   修改key的名称   
RENAMENX key newkey   仅当newkey不存在时，将key该名为newkey   
TYPE key   返回key所储存的值的类型   

##

Redis字符串(String)

