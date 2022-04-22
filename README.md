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

📓 solution, ⚜️ .csproj / project , 📒 solution folder , 📙 folder, 📄 file / code

- **src/ExampleApp(project name)** ⚜️📓

  ExampleApp.sln

  .gitattributes 📄

  .gitignore 📄

  Readme.md 📄

  - **Application** 📒

    - **ExampleApp**⚜️

      program.cs📄

      startup.cs📄

      - **Controllers** 📙

        Contoller.cs📄

      - **ViewModels** 📙

        VM.cs📄

      - **Security** 📙

        AuthorizationApp.cs📄

  - **BoundedContext** 📒

    - **ExampleApp.DataTransformObject** 📚

      - **Main** 📙

        Dto.cs 📄

        ExampleDto.cs 📄

      - **Settings** 📙

        SettingDto.cs 📄

      - **Shared** 📙

        DocumentDto.cs 📄

    - **Repositories** 📒

      - **ExampleApp.Repository.Man** 📚

        - **CountryService** 📙

          ICountryRepository.cs 📄

          CountryRepository.cs 📄

          - **QueryStore** 📙

            CountryStore.cs 📄

        - **OtherService** 📙

          IOtherRepository.cs 📄

          OtherRepository.cs 📄

          - **QueryStore** 📙

            OtherStore.cs 📄

      - **ExampleApp.Repository.Shared**📚

        - **SettingService** 📙

          ISettingRepository.cs 📄

          SettingRepository.cs 📄

  - **Service** 📒

    - **ExampleApp.Service.Meta** 📚

      IMetaService.cs 📄

      MetaService.cs 📄

      - **DependencyInjection** 📙

        MetaICollectionServiceExtensions.cs 📄

      - **Options** 📙

        MetaOptions.cs 📄

        MetaOptionsExtension.cs 📄

      - **Enums** 📙

        Metas.cs 📄

      - **Extesnions** 📙

        MetaServiceExtensions.cs 📄

    - **ExampleApp.Service.Other** 📚

      IOtherService.cs 📄

      OtherService.cs 📄

      - **DependencyInjection** 📙

        OtherCollectionServiceExtensions.cs 📄

  - **Core** 📒

    - **ExampleApp.Core**📚

      Global.cs 📄

      - **Helper**📙

        Helper.cs 📄

      - **Util** 📙

        Util.cs 📄

      - **Enums** 📙

        ExampleAppTypes.cs 📄

      - **Extesnions** 📙

        ExampleApp.cs

    - **Consoles** 📒

      - **ExampleApp.Core.Configure**⚜️

        program.cs 📄

  - **Infrastructure** 📒

    - **Models** 📙

      - **ExampleApp.Infrastructure.Models** 📚

        - **Main** 📙

          Country.cs 📄

          ExampleSet.cs 📄

        - **Settings** 📙

          Setting.cs 📄

        - **Shared** 📙

          Document.cs 📄

      - **ExampleApp.Infrastructure.DataTypes** 📚

        Genderes.cs 📄

    - **DataBases** 📙

      - **ExampleApp.Infrastructure.DataBases.SqlServer**📚

        ExampleAppDbContext.cs 📄

        OtheConfigDatabaseOption.cs 📄

        - **Seed** 📙

          SecuritySeed.cs 📄

          DataSeed.cs 📄

        - **Migrations** 📙

          Snapshot.cs 📄

      - **ExampleApp.Infrastructure.DataBases.JsonDb**📚

        ExampleAppJsonContext.cs 📄

        - **Seed** 📙

          DataSeed.cs 📄

  - **Shared** 📒

    - **ExampleApp.SharedKernel**📚

      - **Base** 📙

        Base.cs 📄

      - **Security** 📙

        SharedSecurity.cs 📄

      - **Enums** 📙

        SharedEnums.cs 📄

      - **ExtensionMethos** 📙

        FunExtensiona.cs 📄

------

## - Note



1. #### This structure need to ``namespace`` management(Fix `namespace` to be more simple).

2. #### [Inject] libs will work perfectly to inject repositories.

3. #### Don't use Repository as Service or vice versa.

4. #### Core and more can be extra Domain, Data,

5. #### This all under ``src`` Folder , ``test`` Folder not implement in this version
