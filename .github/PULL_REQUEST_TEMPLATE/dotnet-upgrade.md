# .NET Upgrade Pull Request

## 📋 Summary

<!-- Brief description of the upgrade performed -->

**Upgrade Type**: Framework Upgrade  
**Source Version**: `net_.0`  
**Target Version**: `net_.0`  

## 📊 Projects Updated

| Project | Before | After | Status |
|---------|--------|-------|--------|
| Project.csproj | net6.0 | net8.0 | ✅ |
| Project.Tests.csproj | net6.0 | net8.0 | ✅ |

## 📦 NuGet Package Changes

### Updated Packages

| Package | Old Version | New Version |
|---------|-------------|-------------|
| Microsoft.Extensions.Logging | 6.0.0 | 8.0.0 |

### Removed Packages (Built into .NET)

- None

### New Packages Added

- None

## 🔧 Code Changes

<!-- List any code changes required for the upgrade -->

- [ ] No code changes required
- [ ] Updated deprecated API calls
- [ ] Fixed breaking changes
- [ ] Updated configuration

### Details

<!-- Describe specific code changes if any -->

## ✅ Validation Results

### Build Verification

```
dotnet build --configuration Release
```

- [ ] Build succeeded with no errors
- [ ] Build succeeded with warnings (see below)
- [ ] Build failed (see errors below)

### Test Results

```
dotnet test --configuration Release
```

- [ ] All tests passed
- [ ] Some tests failed (see below)
- [ ] Tests not run

| Test Project | Total | Passed | Failed | Skipped |
|--------------|-------|--------|--------|---------|
| Project.Tests | 0 | 0 | 0 | 0 |

### Package Audit

- [ ] No vulnerable packages
- [ ] Vulnerable packages found (see below)

## ⚠️ Breaking Changes

<!-- List any breaking changes that required manual fixes -->

- None identified

## 📝 CI/CD Updates

- [ ] GitHub Actions workflows updated
- [ ] Azure DevOps pipelines updated
- [ ] Docker files updated
- [ ] global.json updated
- [ ] No CI/CD changes needed

## 🔙 Rollback Instructions

If issues are discovered after merge:

1. Revert this PR
2. Run `dotnet restore` to restore previous packages
3. Verify build and tests pass

## 📖 References

- [.NET 8 What's New](https://learn.microsoft.com/dotnet/core/whats-new/dotnet-8)
- [Breaking Changes in .NET 8](https://learn.microsoft.com/dotnet/core/compatibility/8.0)
- Related Issue: #

## ✅ Checklist

- [ ] All projects updated to target framework
- [ ] All NuGet packages compatible
- [ ] Build succeeds locally
- [ ] All tests pass
- [ ] CI/CD pipelines updated (if applicable)
- [ ] No security vulnerabilities introduced
- [ ] Documentation updated (if applicable)

---

**Closes**: #
