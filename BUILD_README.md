# PowerToys with Dynamic Updates - GitHub Actions Build

This repository contains PowerToys with enhanced dynamic update functionality for Run plugins.

## What's Changed

### Dynamic Updates Feature
- **MainViewModel.cs**: Enhanced result replacement logic for real-time updates
- **Spotify Plugin**: Implements `IResultUpdated` interface for live music controls

## Building with GitHub Actions

### Automatic Build
The workflow automatically triggers on:
- Push to `main` or `master` branches
- Pull requests
- Manual trigger via "Actions" tab

### Manual Trigger
1. Go to the **Actions** tab in your GitHub repository
2. Select "Build PowerToys with Dynamic Updates"
3. Click "Run workflow"
4. Choose the branch and click "Run workflow"

### Build Artifacts
After successful build, download:
- **powertoys-x64-Release**: Complete PowerToys build
- **spotify-plugin-Release**: The Spotify plugin (if available)

### Build Matrix
- **Platform**: x64 (ARM64 can be added later)
- **Configuration**: Release
- **Runner**: Windows Server 2022

## Testing the Dynamic Updates

1. Download the build artifacts
2. Install PowerToys normally
3. Copy the Spotify plugin to `C:\Program Files\PowerToys\RunPlugins\`
4. Test real-time music control updates

## Build Dependencies
- .NET 9.0
- MSBuild with Visual Studio 2022 tools
- Windows SDK 22621
- NuGet package restoration with caching

## Features Tested
✅ Plugin compilation
✅ Dynamic result replacement
✅ Real-time UI updates
✅ Performance optimizations
