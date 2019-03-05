我们可以在创建容器的时候，将宿主机的目录与容器内的目录进行映射，这样我们就可 以通过修改宿主机某个目录的文件从而去影响容器。
创建容器添加-v参数后边为 宿主机目录:容器目录，例如:

` docker run ‐di ‐v /usr/local/myhtml:/usr/local/myhtml ‐‐name=mycentos3 centos:7`

如果你共享的是多级的目录，可能会出现权限不足的提示。 

这是因为CentOS7中的安全模块selinux把权限禁掉了，我们需要添加参数 --privileged=true 来解决挂载的目录没有权限的问题.