FROM mcr.microsoft.com/dotnet/sdk:7.0 as build
LABEL org.opencontainers.image.description="worker"\
    org.opencontainers.image.authors="CristianSigel"
WORKDIR /source
COPY *.csproj /source
RUN dotnet restore
COPY . /source
RUN dotnet publish -c release -o /app --no-restore

FROM mcr.microsoft.com/dotnet/runtine:7.0
WORKDIR /app
COPY --from=build /app .
ENTRYPOINT [ "dotnet", "Worker.ddl" ]