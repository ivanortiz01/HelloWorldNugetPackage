# HelloWorldNugetPackage
This repository has a proof of concept about publish package to azure devops artifacts and use in a console app

Generated a feed in azure devops artifacts.

Comand to create package:

dotnet pack

You can configurate, when the build of the application accours, generate the package:

dotnet build

Commands to push package to nuget artifacts.

dotnet restore --interactive

dotnet nuget push .\bin\Debug\HelloWorldLibrary.1.0.0.nupkg  --source "HelloWorld_Feed" --api-key "HelloWorld_Feed_Library" --interactive

Base on this articles:

https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-the-dotnet-cli

https://camargo-wes.medium.com/how-to-send-net-core-nuget-packages-to-azure-artifacts-238fa08db6b5

https://docs.microsoft.com/es-es/azure/devops/artifacts/nuget/consume?view=azure-devops