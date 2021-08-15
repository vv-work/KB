# Jupyter

## PowrShell Jupyter
Its based on top of DotNet [Interactive](https://github.com/dotnet/interactive)


```PowerShell
jupyter kernelspec list

dotnet tool install -g --add-source "https://pkgs.dev.azure.com/dnceng/public/_packaging/dotnet-tools/nuget/v3/index.json" Microsoft.dotnet-interactive

dotnet interactive jupyter install

```

### Remote Access


```powershell 
jupyter notebook --generate-config
```

