FROM mcr.microsoft.com/dotnet/core/aspnet:3.1
WORKDIR /app
#时区更改
RUN /bin/sh -c 'ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime'
#数据文件夹映射到宿主机，防止重启之后配置和数据丢失
VOLUME /MyData

ENTRYPOINT ["sh", "run.sh"]
