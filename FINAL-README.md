# AniLiberty Streaming Provider for Seanime

## 🎯 Project Overview

This project creates a streaming provider for Seanime that integrates with the Russian anime service **AniLiberty** (https://aniliberty.top). It allows Seanime users to access Russian anime content directly through their familiar Seanime interface.

## 📁 Project Structure

```
Seanime-streaming-providers/
├── src/
│   └── AniLiberty/
│       └── manifest.json          # Main provider implementation
├── README-AniLiberty.md           # Comprehensive documentation
├── INSTALL-AniLiberty.md          # Installation guide
├── example-usage.md               # Usage examples and flow
├── ANILIBERTY-SUMMARY.md          # Technical implementation summary
├── test-aniliberty.js             # API testing script
└── FINAL-README.md                # This overview file
```

## 🚀 Quick Start

### Installation
1. Copy `src/AniLiberty/` to your Seanime extensions directory
2. Restart Seanime
3. Enable "AniLiberty" in Settings → Extensions → Streaming Providers

### Usage
1. Search for anime in Seanime
2. Select AniLiberty as the source
3. Choose an episode
4. Enjoy Russian anime streams!

## ✨ Key Features

- **🔍 Smart Search**: Direct integration with AniLiberty's search API
- **📺 Multiple Qualities**: 480p, 720p, and 1080p HLS streams
- **🇷🇺 Russian Content**: Access to Russian-dubbed anime library
- **⚡ Fast Performance**: Optimized API calls and response handling
- **🛡️ Error Handling**: Graceful handling of network issues and missing content
- **🎯 No Authentication**: Works without registration

## 🔧 Technical Details

### API Integration
- **Base URL**: `https://aniliberty.top/api/v1`
- **Search**: `GET /app/search/releases?query={query}`
- **Releases**: `GET /anime/releases/{idOrAlias}`
- **Streams**: Direct HLS URLs from episode data

### Provider Configuration
```typescript
{
  id: "aniliberty",
  name: "AniLiberty", 
  language: "ru",
  supportsDub: false,
  episodeServers: ["AniLiberty Server"]
}
```

## 📚 Documentation

| File | Purpose |
|------|---------|
| `README-AniLiberty.md` | Complete feature documentation |
| `INSTALL-AniLiberty.md` | Step-by-step installation guide |
| `example-usage.md` | Usage examples and user flow |
| `ANILIBERTY-SUMMARY.md` | Technical implementation details |
| `test-aniliberty.js` | API testing and validation |

## 🎬 Supported Content

- **Languages**: Russian (primary), English, Japanese
- **Types**: TV series, movies, OVAs, specials
- **Qualities**: 480p, 720p, 1080p
- **Format**: HLS streams (m3u8)

## 🔍 Search Capabilities

- Query normalization for better results
- Support for multiple title formats
- Automatic fallback to alternative titles
- Error handling for no results

## 📺 Streaming Features

- **Quality Selection**: Automatic best quality detection
- **HLS Support**: Native m3u8 stream compatibility
- **Headers**: Proper streaming headers for compatibility
- **Fallback**: Graceful degradation for unavailable streams

## 🛠️ Development

### Prerequisites
- Node.js (for testing)
- Seanime installation
- Understanding of TypeScript/JavaScript

### Testing
```bash
# Install dependencies
npm install node-fetch

# Run API tests
node test-aniliberty.js
```

### Customization
The provider can be customized by modifying:
- Search query normalization
- Quality selection logic
- Error handling behavior
- Request headers

## 🌍 Limitations

- **Geographic Restrictions**: May be limited to certain regions
- **Content Availability**: Depends on AniLiberty's library
- **Language**: Primarily Russian content
- **API Dependencies**: Subject to AniLiberty's policies

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project follows the same license as the Seanime streaming providers project.

## 🆘 Support

### Common Issues
- **Provider not appearing**: Check installation directory and restart Seanime
- **Search not working**: Verify internet connection and try different terms
- **Streams not loading**: Check HLS player support and firewall settings

### Getting Help
1. Check the troubleshooting sections in documentation
2. Verify Seanime version compatibility
3. Check Seanime logs for specific errors
4. Create an issue with detailed information

## 🎉 Success Metrics

This provider successfully:
- ✅ Integrates with AniLiberty's API
- ✅ Provides Russian anime content to Seanime users
- ✅ Supports multiple quality streams
- ✅ Handles errors gracefully
- ✅ Follows Seanime provider standards
- ✅ Includes comprehensive documentation

## 🔮 Future Enhancements

Potential improvements:
- Result caching for better performance
- Advanced search filters
- User preference memory
- Offline episode list caching
- Alternative search methods

---

**Created by**: cuteceo  
**Version**: 1.0.0  
**Last Updated**: 2024  
**Status**: Ready for use 