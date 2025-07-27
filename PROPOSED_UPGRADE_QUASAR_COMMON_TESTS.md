# Proposal: Upgrade Quasar.Common.Tests

This document outlines a possible approach to modernize the `Quasar.Common.Tests` project.

## Rationale

The test project currently targets **.NET Framework 4.6.2**. Updating to a supported version of .NET provides:

- Access to modern language features
- Improved performance of the test runner
- Compatibility with the rest of the solution once other projects are upgraded

## Suggested changes

1. **Target Framework**
   - Switch to `net8.0` using the `Microsoft.NET.Sdk`.
2. **Package Updates**
   - Update `Microsoft.NET.Test.Sdk`, `MSTest.TestAdapter` and `MSTest.TestFramework` to their latest stable releases.
3. **Build System**
   - Use the current `dotnet` CLI tooling for building and running the unit tests.
4. **Code Adjustments**
   - Replace any APIs removed in modern .NET versions and update references as necessary.

## Benefits

- Unified tooling and framework version across all projects
- Faster and more reliable test execution

## Considerations

- Running tests will require the .NET 8 SDK.
- Verify that test output paths and project references continue to work under the updated SDK.
