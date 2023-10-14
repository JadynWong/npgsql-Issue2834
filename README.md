Reproduce https://github.com/npgsql/efcore.pg/issues/2834

Change `connectionString` for you. Run `ConsoleApp1`.

```bash
dotnet run  --project .\ConsoleApp1\ConsoleApp1.csproj
```

```log
Unhandled exception. System.TypeLoadException: Could not load type 'System.Data.Common.DbDataSource' from assembly 'Npgsql, Version=7.0.6.0, Culture=neutral, PublicKeyToken=5d8b90d52f46fda7'.
   at Test.Run(String connectionString)
   at Program.<Main>$(String[] args) in D:\demo\Issue2834\ConsoleApp1\Program.cs:line 4
```

```bash
.NET SDK:
 Version:   7.0.402
 Commit:    791db8e2d8

运行时环境:
 OS Name:     Windows
 OS Version:  10.0.22631
 OS Platform: Windows
 RID:         win10-x64
 Base Path:   C:\Program Files\dotnet\sdk\7.0.402\

Host:
  Version:      8.0.0-rc.2.23479.6
  Architecture: x64
  Commit:       0b25e38ad3

.NET SDKs installed:
  6.0.415 [C:\Program Files\dotnet\sdk]
  7.0.402 [C:\Program Files\dotnet\sdk]
  8.0.100-rc.2.23502.2 [C:\Program Files\dotnet\sdk]

.NET runtimes installed:
  Microsoft.AspNetCore.App 6.0.23 [C:\Program Files\dotnet\shared\Microsoft.AspNetCore.App]
  Microsoft.AspNetCore.App 7.0.12 [C:\Program Files\dotnet\shared\Microsoft.AspNetCore.App]
  Microsoft.AspNetCore.App 8.0.0-rc.2.23480.2 [C:\Program Files\dotnet\shared\Microsoft.AspNetCore.App]
  Microsoft.NETCore.App 6.0.23 [C:\Program Files\dotnet\shared\Microsoft.NETCore.App]
  Microsoft.NETCore.App 7.0.12 [C:\Program Files\dotnet\shared\Microsoft.NETCore.App]
  Microsoft.NETCore.App 8.0.0-rc.2.23479.6 [C:\Program Files\dotnet\shared\Microsoft.NETCore.App]
  Microsoft.WindowsDesktop.App 6.0.23 [C:\Program Files\dotnet\shared\Microsoft.WindowsDesktop.App]
  Microsoft.WindowsDesktop.App 7.0.12 [C:\Program Files\dotnet\shared\Microsoft.WindowsDesktop.App]
  Microsoft.WindowsDesktop.App 8.0.0-rc.2.23479.10 [C:\Program Files\dotnet\shared\Microsoft.WindowsDesktop.App]

Other architectures found:
  x86   [C:\Program Files (x86)\dotnet]
    registered at [HKLM\SOFTWARE\dotnet\Setup\InstalledVersions\x86\InstallLocation]

Environment variables:
  Not set

global.json file:
  D:\demo\Issue2834\global.json

Learn more:
  https://aka.ms/dotnet/info

Download .NET:
  https://aka.ms/dotnet/download

```