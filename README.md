# dotnetrun
## dotnet core docker运行环境
对于需要频繁发布和测试的应用，docker的更新是在有点麻烦，于是做了这个镜像，将镜像的/app文件夹映射到宿主，这样只需要更新宿主的文件后重启docker实例即可完成更新。
* 也可以用于centos6这类利用docker运行core应用
* 需在映射的文件夹中加入一个run.sh脚本来启动实际应用，已有例子
## 其他改动
* 默认为北京时间
* 创建/MyData VOLUME

## 运行示例
	docker run --name myapp --restart on-failure:5 --privileged=true -v ./data:/MyData -v ./appbin:/app -d vanjoge/dotnetrun