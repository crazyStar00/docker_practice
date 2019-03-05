我们可以通过以下命令查看容器运行的各种数据
`docker inspect 容器名称(容器ID) `

也可以直接执行下面的命令直接输出IP地址 
`docker inspect ‐‐format='{{.NetworkSettings.IPAddress}}' 容器名称(容器ID)`