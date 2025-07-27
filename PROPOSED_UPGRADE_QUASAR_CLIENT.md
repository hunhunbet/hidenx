# Proposal: Upgrade Quasar.Client

This document outlines an approach to update the `Quasar.Client` project to a more current .NET platform.

## Rationale

The client currently targets **.NET Framework 4.6.2**. Moving to a supported version of .NET provides:

- Ongoing security patches
- Access to the latest language features
- Potential performance gains

## Suggested changes

1. **Target Framework**
   - Switch to `net8.0-windows` using the `Microsoft.NET.Sdk.WindowsDesktop` SDK with WinForms enabled.
2. **Package Updates**
   - Update NuGet packages such as `ILRepack.Lib.MSBuild.Task`, `MouseKeyHook`, `Portable.BouncyCastle` and `protobuf-net` to their most recent stable releases.
3. **Build System**
   - Use the current `dotnet` CLI tooling for building and packaging the client.
4. **Testing**
   - Compile and run unit tests under the new framework. Replace any deprecated APIs encountered during migration.

## Benefits

- Easier maintenance and compatibility with modern tooling
- Improved support for recent Windows versions
- Better performance characteristics

## Considerations

- Users will require the .NET 8 Desktop Runtime installed to run the updated client.
- Address breaking changes in dependencies during the upgrade.
