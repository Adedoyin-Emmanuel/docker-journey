FROM bitnami/dotnet-sdk:latest

WORKDIR /app

COPY . .

RUN dotnet build

CMD ["dotnet", "run", "Program.cs"]
