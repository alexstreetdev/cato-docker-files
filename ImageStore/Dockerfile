FROM microsoft/dotnet:2.1-sdk as builder

RUN git clone https://github.com/alexstreetdev/ImageStore.git

WORKDIR ./ImageStore/ImageStore

RUN dotnet restore ImageStore.csproj

FROM builder as publish
RUN dotnet publish -c release -o output

FROM microsoft/dotnet:2.1-aspnetcore-runtime AS runtime

WORKDIR /img

COPY --from=publish ./ImageStore/ImageStore/output ./

ENTRYPOINT ["dotnet", "ImageStore.dll"]
