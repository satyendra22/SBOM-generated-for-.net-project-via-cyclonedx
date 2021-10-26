# SBOM generated for .net project via cyclonedx 
SBOM generated for .net project via cyclonedx

- Clone and complie https://github.com/CycloneDX/cyclonedx-dotnet project to generate CycloneDX.exe
  - Download cyclonedx-dotnet code and import to visual studio code
  - Unzip cyclonedx-dotnet-master.zip and use Visual Studio 2019 to open CycloneDX.sln. There are 5 projects in this program. Just compile (clt+sft+B) the CycloneDX project in it.     Do not build or rebuild or compile the entire program, otherwise there will be a lot of errors.
  - After compilation we got CycloneDX.exe   under project path [cyclonedx-dotnet\CycloneDX\bin\Debug\netcoreapp3.1\publish\CycloneDX.exe]
 
-  Setup any .net project for generate SBOM
    - Setup test project https://github.com/satyendra22/project-aspnet-dotnet-webapp
  
-  Use CyCloneDX.exe to generate BOM for the test plan
    - Syntax: CycloneDX <path> -o <OUTPUT_DIRECTORY>  (path is the directory of .sln, .csproj, .vbproj, or packages.config)
    - <code> C:\<CODE>\cyclonedx-dotnet\CycloneDX\bin\Debug\netcoreapp3.1\publish> .\CycloneDX.exe C:\<Proj-Code>project-aspnet-dotnet-webapp\SampleWebApplication -o C:\<OUTPATH>\project-aspnet-dotnet-webapp\BOM' </code>
    - BOM.xml is generated in output directory. generated file added for reference https://github.com/satyendra22/SBOM-generated-for-.net-project-via-cyclonedx/blob/main/bom.xml
