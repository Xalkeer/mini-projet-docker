# Stage 1 : build
FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build

WORKDIR /src

# Copier le projet
COPY Worker.csproj ./
RUN dotnet restore Worker.csproj

# Copier le reste du code
COPY . ./

# Publier explicitement le projet
RUN dotnet publish Worker.csproj -c Release --self-contained false -o /app/publish

# Stage 2 : runtime
FROM mcr.microsoft.com/dotnet/runtime:7.0

WORKDIR /app
COPY --from=build /app/publish .

CMD ["dotnet", "Worker.dll"]
