# Proposal: Upgrade Quasar.Server

This document summarizes a possible approach to update the `Quasar.Server` project to a modern .NET version.

## Rationale

The server currently targets **.NET Framework 4.6.2**. Upgrading to the latest LTS of .NET brings:

- Long term support and security updates
- Access to modern language features
- Improved performance

## Suggested changes

1. **Target Framework**
   - Migrate the project to `net8.0-windows` using the `Microsoft.NET.Sdk.WindowsDesktop` SDK with WinForms enabled.
2. **Package Updates**
   - Update NuGet dependencies to their latest stable versions. Examples include `Mono.Cecil`, `protobuf-net`, `Open.Nat` and `Portable.BouncyCastle`.
3. **Build System**
   - Use the latest `dotnet` CLI tooling for builds and packaging.
4. **Testing**
   - Ensure unit tests compile under the updated framework. Replace deprecated APIs as needed.

## Benefits

- Easier maintenance with modern tooling
- Better support for new Windows versions
- Potential performance improvements

## Considerations

- Users will need the .NET 8 Desktop Runtime installed to run the server.
- Any breaking changes in updated packages must be addressed during migration.

