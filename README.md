# gitlab+sonarqube - swarm 部署

## 使用
### 修改 gitlab 的 hostname
```yml
gitlab: 
    image: gitlab/gitlab-ce:12.4.2-ce.0
    hostname: gitlab.hanlyjiang.cn
```

### 给需要运行gitlab的node加标签
> docker-desktop 替换为自己的
```
docker node update --label-add level=high docker-desktop 
```

### 启动
```
docker stack deploy -c docker-compose.yml codemgr
```

## 服务地址
> 请将ip替换为对应的地址    
* sonarqube: http://localhost:9000
* gitlab: http://localhost
* visualizer: http://localhost:8081
* 数据库测试：http://localhost:8080