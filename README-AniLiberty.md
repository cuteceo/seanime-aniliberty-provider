# AniLiberty Streaming Provider for Seanime

## Overview

This is a streaming provider for Seanime that integrates with the Russian anime streaming service AniLiberty (https://aniliberty.top). It provides access to high-quality Russian anime streams with multiple quality options.

## Features

- **Russian Anime Content**: Access to a large library of Russian-dubbed and subbed anime
- **Multiple Quality Streams**: Support for 480p, 720p, and 1080p HLS streams
- **Fast Search**: Direct integration with AniLiberty's search API
- **Episode Management**: Automatic episode detection and sorting
- **No Authentication Required**: Works without user registration

## Installation

1. Copy the `AniLiberty` folder to your Seanime streaming providers directory
2. Restart Seanime
3. The AniLiberty provider will appear in your streaming sources list

## API Integration

This provider uses the official AniLiberty API v1:

- **Base URL**: `https://aniliberty.top/api/v1`
- **Search Endpoint**: `/app/search/releases?query={query}`
- **Release Details**: `/anime/releases/{idOrAlias}`
- **Episode Streams**: Direct HLS stream URLs from episode data

## Supported Features

### Search
- Query normalization for better search results
- Support for Russian, English, and original titles
- Automatic fallback to alternative title formats

### Episodes
- Automatic episode detection from release data
- Episode sorting by ordinal/sort order
- Support for special episodes and OVAs

### Streaming
- HLS stream support (m3u8 format)
- Multiple quality options (480p, 720p, 1080p)
- Automatic quality selection based on availability
- Proper headers for streaming compatibility

## Technical Details

### Provider Settings
- **Episode Servers**: "AniLiberty Server"
- **Dub Support**: False (Russian-focused service)
- **Language**: Russian (ru)

### Request Headers
- User-Agent: Modern browser user agent
- Accept-Language: Russian preferred
- Referer: Set to aniliberty.top for API compatibility

### Error Handling
- Graceful handling of missing episodes
- Proper error messages for failed requests
- Fallback mechanisms for search queries

## Usage

1. **Search for Anime**: Use the search function to find anime by title
2. **Select Episode**: Choose from available episodes
3. **Start Streaming**: The provider will automatically select the best available quality

## Limitations

- **Language**: Primarily Russian content (some English titles available)
- **Dub Only**: Most content is Russian-dubbed
- **Geographic Restrictions**: May be limited to certain regions
- **API Rate Limits**: Subject to AniLiberty's API usage policies

## Troubleshooting

### Common Issues

1. **No Results Found**
   - Try using the original Japanese title
   - Check spelling and remove special characters
   - Use shorter search terms

2. **Streaming Issues**
   - Check your internet connection
   - Try a different quality setting
   - Ensure your player supports HLS streams

3. **Episode Not Found**
   - Verify the anime has been released on AniLiberty
   - Check if the episode number is correct
   - Try refreshing the episode list

## Contributing

To contribute to this provider:

1. Fork the repository
2. Make your changes
3. Test thoroughly with different anime titles
4. Submit a pull request

## License

This provider is released under the same license as the Seanime streaming providers project.

## Support

For issues specific to this provider, please create an issue in the repository. For general Seanime support, refer to the main Seanime documentation.

## Changelog

### Version 1.0.0
- Initial release
- Basic search and streaming functionality
- Support for multiple quality streams
- Russian language support 