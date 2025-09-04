## 🔢 Semantic Versioning (SemVer)

Guidelines for version numbering following the Semantic Versioning specification.

### 📏 Version Format
All versions must follow the format: `MAJOR.MINOR.PATCH`

- **MAJOR**: Incremented for breaking changes that are not backward compatible
- **MINOR**: Incremented for new features that are backward compatible
- **PATCH**: Incremented for backward compatible bug fixes

### 🏷️ Version Types

#### 🚀 Major Version (X.0.0)
- Breaking changes to existing functionality
- API changes that break backward compatibility
- Removal of deprecated features
- Significant architectural changes

#### ✨ Minor Version (0.X.0)
- New features that are backward compatible
- New functionality additions
- Enhancements to existing features
- Non-breaking API additions

#### 🔧 Patch Version (0.0.X)
- Bug fixes and error corrections
- Security patches
- Performance improvements
- Documentation updates
- Code refactoring without behavior changes

### 📋 Pre-release Versions
For development versions, use suffixes:
- `1.0.0-alpha` - Early development
- `1.0.0-beta` - Feature complete, testing phase
- `1.0.0-rc` - Release candidate

### ✨ Examples

```bash
# Starting a new project
v1.0.0

# Adding a new feature
v1.1.0

# Fixing a bug
v1.1.1

# Breaking change
v2.0.0

# Pre-release versions
v1.2.0-alpha
v1.2.0-beta.1
v1.2.0-rc.1
```

### 🎯 Best Practices

#### ✅ Do:
- Start with version `1.0.0` for initial release
- Always increment only one number at a time
- Reset lower numbers when incrementing higher ones
- Use consistent version format across all releases
- Document breaking changes in release notes

#### ❌ Don't:
- Skip version numbers
- Use arbitrary version numbers
- Increment major version for minor changes
- Forget to update version in all relevant files

### 🔗 Integration with Workflow

#### Branch Names:
```bash
# Release branch with version
git checkout -b release/5/v1.2.0

# Hotfix branch with version  
git checkout -b hotfix/8/fix-auth-v1.1.1
```

#### Commit Messages:
```bash
# Release commit
git commit -m "🔖 release: new version; v1.2.0"

# Hotfix commit
git commit -m "🔥 hotfix: fix auth issue; v1.1.1"
```