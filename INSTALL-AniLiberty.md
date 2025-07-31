# Installing AniLiberty Provider for Seanime

## Quick Installation

### Step 1: Download the Provider
1. Navigate to the `Seanime-streaming-providers/src/AniLiberty/` folder
2. Copy the entire `AniLiberty` folder

### Step 2: Install in Seanime
1. Open your Seanime installation directory
2. Navigate to the streaming providers folder (usually `extensions/streaming-providers/` or similar)
3. Paste the `AniLiberty` folder here
4. Restart Seanime

### Step 3: Enable the Provider
1. Open Seanime
2. Go to Settings → Extensions → Streaming Providers
3. Find "AniLiberty" in the list
4. Enable it if it's not already enabled

## Manual Installation

If the quick installation doesn't work, you can manually install:

1. **Locate Seanime Extensions Directory**
   - Windows: `%APPDATA%/Seanime/extensions/streaming-providers/`
   - macOS: `~/Library/Application Support/Seanime/extensions/streaming-providers/`
   - Linux: `~/.config/Seanime/extensions/streaming-providers/`

2. **Copy Files**
   ```bash
   cp -r AniLiberty/ /path/to/seanime/extensions/streaming-providers/
   ```

3. **Set Permissions** (Linux/macOS)
   ```bash
   chmod 755 /path/to/seanime/extensions/streaming-providers/AniLiberty/
   chmod 644 /path/to/seanime/extensions/streaming-providers/AniLiberty/manifest.json
   ```

## Verification

To verify the installation:

1. Restart Seanime completely
2. Go to Settings → Extensions → Streaming Providers
3. You should see "AniLiberty" in the list
4. Try searching for an anime (e.g., "Naruto")
5. Select AniLiberty as the source
6. You should see Russian anime results

## Troubleshooting

### Provider Not Appearing
- Check that the folder is in the correct directory
- Verify the manifest.json file is present and valid
- Restart Seanime completely
- Check Seanime logs for errors

### Search Not Working
- Verify your internet connection
- Check if AniLiberty is accessible from your location
- Try searching with different terms
- Check Seanime logs for API errors

### Streaming Issues
- Ensure your media player supports HLS streams
- Check if the anime is available on AniLiberty
- Try different quality settings
- Verify your firewall isn't blocking the streams

## Support

If you encounter issues:

1. Check the main README-AniLiberty.md for detailed information
2. Verify your Seanime version is compatible
3. Check Seanime logs for specific error messages
4. Create an issue in the repository with:
   - Seanime version
   - Operating system
   - Error messages from logs
   - Steps to reproduce the issue

## Uninstallation

To remove the AniLiberty provider:

1. Go to Settings → Extensions → Streaming Providers
2. Disable AniLiberty
3. Delete the `AniLiberty` folder from the extensions directory
4. Restart Seanime 