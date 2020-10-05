执行下面的命令构建镜像并启动服务：

```undefined
docker-compose up -d
```

进入ansible容器

```bash
docker-compose exec ansible sh
```

执行下面命令：

```text
ssh-copy-id app
ssh-copy-id db
ssh-copy-id web
```

> 会提示输入密码，密码是`root`

## 使用

我们使用ping命令测试一下：

```undefined
ansible dev -m ping
```

输出类似下面的信息：

```jsx
host1 | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3.7"
    },
    "changed": false,
    "ping": "pong"
}

host2 | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3.7"
    },
    "changed": false,
    "ping": "pong"
}
```



作者：redexpress
链接：https://www.jianshu.com/p/2ce2dd2c4141
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。