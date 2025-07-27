# Proposal: Upgrade Quasar.Common

This document outlines a possible approach to update the `Quasar.Common` library to a modern .NET version.

## Rationale

The library currently targets **.NET Framework 4.6.2**. Upgrading to a supported .NET release provides:

- Long term support and security patches
- Access to recent language features
- Better performance and compatibility with modern tooling

## Suggested changes

1. **Target Framework**
   - Migrate the project to `net8.0` using the `Microsoft.NET.Sdk`.
2. **Package Updates**
   - Bring NuGet dependencies such as `EnterpriseLibrary.Common`, `Newtonsoft.Json` and `protobuf-net` to their latest stable versions.
3. **Build System**
   - Use the current `dotnet` CLI for building and packaging the library.
4. **Testing**
   - Run the unit tests on the new framework and update code to replace any deprecated APIs.

## Benefits

- Simplified maintenance with a supported .NET version
- Improved runtime performance
- Compatibility with the upgraded client and server components

## Considerations

- The library will require .NET 8 to build and run.
- Any breaking changes in dependencies must be resolved during migration.
