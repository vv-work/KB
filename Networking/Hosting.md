# IIS 

> It take me a while to thing about all possibilities . But quite obviously IIS wind


## Quick IIS Net .Core hosting
1. Install Net Core hosting Bandle
    - (page)[https://dotnet.microsoft.com/download/dotnet-core/thank-you/runtime-aspnetcore-3.1.9-windows-hosting-bundle-installer]

## Unity
1. Article about "new" Compression
            And I really did suffer hard to make it work on IIS so I will left that time of improment for letter 
            for now Decompression Fall back is good enoug
(Ling to artilce WebGL 2020.1)[https://forum.unity.com/threads/changes-to-the-webgl-loader-and-templates-introduced-in-unity-2020-1.817698/]


### Compression Fallback working fine for me 

```csharp
<?xml version="1.0" encoding="UTF-8"?>
<configuration>
    <system.webServer>
        <staticContent>
            <remove fileExtension=".unityweb" />
            <mimeMap fileExtension=".unityweb" mimeType="application/octet-stream" />
            <remove fileExtension=".wasm" />
            <mimeMap fileExtension=".wasm" mimeType="application/wasm" />
        </staticContent>
        <rewrite>
            <outboundRules>
                <rule name="Append gzip Content-Encoding header">
                    <match serverVariable="RESPONSE_Content-Encoding" pattern=".*" />
                    <conditions>
                        <add input="{REQUEST_FILENAME}" pattern="\.(unityweb|wasm)$" />
                    </conditions>
                    <action type="Rewrite" value="gzip" />
                </rule>
            </outboundRules>
        </rewrite>
    </system.webServer>
</configuration>
```