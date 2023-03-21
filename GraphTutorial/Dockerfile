FROM mcr.microsoft.com/dotnet/sdk:6.0 AS runtime
ENV ASPNETCORE_URLS=https://*:443;http://*:80
WORKDIR /app
RUN dotnet dev-certs https
RUN dotnet dev-certs https --trust
COPY published/ ./
ENTRYPOINT ["dotnet", "GraphTutorial.dll", "ASPNETCORE_URLS=$ASPNETCORE_URLS"]
