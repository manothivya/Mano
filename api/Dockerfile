# set base image 
FROM mcr.microsoft.com/dotnet/sdk:6.0 as build 

WORKDIR /app

COPY *.csproj .
RUN dotnet restore 

copy . .

RUN dotnet publish -c Release -o /app/out

#set runtime image 
FROM mcr.microsoft.com/dotnet/aspnet:6.0 as runtime

WORKDIR /app

COPY --from=build /app/out .

EXPOSE 80

ENTRYPOINT ["dotnet" ,"api.dll"]