# Projects Architecture

------

## - Roles

- Always make sure to build or use ``Dependency Injection`` right.
- Never underestimate the **Secure/Security** layer, take good care of it and customize it.
- Rely on building classes methods have `virtual` keyword .
- Use AspNetCore [source code](https://github.com/dotnet/aspnetcore/tree/main/src) to learn how to correct way to build..
- Test new service with other old services.
- Be dotnet**er** to here and follow new tech added to dotnet.
- Don't take sayings about "Clean Code" against you.
- Code more lines with security and  optimizing  better than write stupide  line.
- If you are new with dotnet or any framework soo do not trust with your intuition with ``Benchmark`` and ``performance``.
- Complicating matters to shorten lines or to implement a new mechanism does not solve the matter, but rather makes the matter worse.
- Remember, you are not the only one who will use this structure, support your code with documents and explanations and make it closer to the framework.
- There are more correct ones that are not revealed to the public, do not believe everything you see on the Internet, most of them are for beginners.

## - Basic File Structure  Asp Net Core Api

ð solution, âï¸ .csproj / project , ð solution folder , ð folder, ð file / code

- **src/ExampleApp(project name)** âï¸ð

  ExampleApp.sln

  .gitattributes ð

  .gitignore ð

  Readme.md ð

  - **Application** ð

    - **ExampleApp**âï¸

      program.csð

      startup.csð

      - **Controllers** ð

        Contoller.csð

      - **ViewModels** ð

        VM.csð

      - **Security** ð

        AuthorizationApp.csð

  - **BoundedContext** ð

    - **ExampleApp.DataTransformObject** ð

      - **Main** ð

        Dto.cs ð

        ExampleDto.cs ð

      - **Settings** ð

        SettingDto.cs ð

      - **Shared** ð

        DocumentDto.cs ð

    - **Repositories** ð

      - **ExampleApp.Repository.Man** ð

        - **CountryService** ð

          ICountryRepository.cs ð

          CountryRepository.cs ð

          - **QueryStore** ð

            CountryStore.cs ð

        - **OtherService** ð

          IOtherRepository.cs ð

          OtherRepository.cs ð

          - **QueryStore** ð

            OtherStore.cs ð

      - **ExampleApp.Repository.Shared**ð

        - **SettingService** ð

          ISettingRepository.cs ð

          SettingRepository.cs ð

  - **Service** ð

    - **ExampleApp.Service.Meta** ð

      IMetaService.cs ð

      MetaService.cs ð

      - **DependencyInjection** ð

        MetaICollectionServiceExtensions.cs ð

      - **Options** ð

        MetaOptions.cs ð

        MetaOptionsExtension.cs ð

      - **Enums** ð

        Metas.cs ð

      - **Extesnions** ð

        MetaServiceExtensions.cs ð

    - **ExampleApp.Service.Other** ð

      IOtherService.cs ð

      OtherService.cs ð

      - **DependencyInjection** ð

        OtherCollectionServiceExtensions.cs ð

  - **Core** ð

    - **ExampleApp.Core**ð

      Global.cs ð

      - **Helper**ð

        Helper.cs ð

      - **Util** ð

        Util.cs ð

      - **Enums** ð

        ExampleAppTypes.cs ð

      - **Extesnions** ð

        ExampleApp.cs

    - **Consoles** ð

      - **ExampleApp.Core.Configure**âï¸

        program.cs ð

  - **Infrastructure** ð

    - **Models** ð

      - **ExampleApp.Infrastructure.Models** ð

        - **Main** ð

          Country.cs ð

          ExampleSet.cs ð

        - **Settings** ð

          Setting.cs ð

        - **Shared** ð

          Document.cs ð

      - **ExampleApp.Infrastructure.DataTypes** ð

        Genderes.cs ð

    - **DataBases** ð

      - **ExampleApp.Infrastructure.DataBases.SqlServer**ð

        ExampleAppDbContext.cs ð

        OtheConfigDatabaseOption.cs ð

        - **Seed** ð

          SecuritySeed.cs ð

          DataSeed.cs ð

        - **Migrations** ð

          Snapshot.cs ð

      - **ExampleApp.Infrastructure.DataBases.JsonDb**ð

        ExampleAppJsonContext.cs ð

        - **Seed** ð

          DataSeed.cs ð

  - **Shared** ð

    - **ExampleApp.SharedKernel**ð

      - **Base** ð

        Base.cs ð

      - **Security** ð

        SharedSecurity.cs ð

      - **Enums** ð

        SharedEnums.cs ð

      - **ExtensionMethos** ð

        FunExtensiona.cs ð

------

## - Note



1. #### This structure need to ``namespace`` management(Fix `namespace` to be more simple).

2. #### [Inject] libs will work perfectly to inject repositories.

3. #### Don't use Repository as Service or vice versa.

4. #### Core and more can be extra Domain, Data,

5. #### This all under ``src`` Folder , ``test`` Folder not implement in this version
