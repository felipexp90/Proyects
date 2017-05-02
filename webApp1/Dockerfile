FROM microsoft/dotnet:latest

WORKDIR /root/
ADD ./app/ ./app/
WORKDIR /root/app

RUN dotnet restore
RUN dotnet build

EXPOSE 63578/tcp 

ENTRYPOINT ["dotnet", "run", "--server.urls", "http://192.168.99.100:63578"]

