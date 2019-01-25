# DevOpsBuildFailureRepro
Minimal Repro of Azure DevOps build failures with .Net core 2.2 and MS Test projects.

This project does reproduce the Azure DevOps build problem with .Net core 2.2
```
2019-01-25T17:43:36.3668681Z ##[warning]MSTestProject\MSTestProject.csproj(0,0): Warning NU1604: Project dependency Microsoft.NETCore.App does not contain an inclusive lower bound. Include a lower bound in the dependency version to ensure consistent restore results.
2019-01-25T17:43:36.3677628Z D:\a\1\s\MSTestProject\MSTestProject.csproj : warning NU1604: Project dependency Microsoft.NETCore.App does not contain an inclusive lower bound. Include a lower bound in the dependency version to ensure consistent restore results.
2019-01-25T17:43:36.3944076Z ##[error]MSTestProject\MSTestProject.csproj(0,0): Error : NETSDK1061: The project was restored using Microsoft.NETCore.App version 1.0.0, but with current settings, version 2.0.0 would be used instead. To resolve this issue, make sure the same settings are used for restore and for subsequent operations such as build or publish. Typically this issue can occur if the RuntimeIdentifier property is set during build or publish but not during restore. For more information, see https://aka.ms/dotnet-runtime-patch-selection.
2019-01-25T17:43:36.3952399Z D:\a\1\s\MSTestProject\MSTestProject.csproj : error : NETSDK1061: The project was restored using Microsoft.NETCore.App version 1.0.0, but with current settings, version 2.0.0 would be used instead. To resolve this issue, make sure the same settings are used for restore and for subsequent operations such as build or publish. Typically this issue can occur if the RuntimeIdentifier property is set during build or publish but not during restore. For more information, see https://aka.ms/dotnet-runtime-patch-selection.
2019-01-25T17:43:36.4363349Z Done Building Project "D:\a\1\s\MSTestProject\MSTestProject.csproj" (default targets) -- FAILED.
2019-01-25T17:43:36.4704580Z Done Building Project "D:\a\1\s\MSTestProject.sln" (default targets) -- FAILED.
```
