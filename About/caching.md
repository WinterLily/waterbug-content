# 2. Caching

Waterbug's caching system is designed for maximum performance while remaining memory-efficient.

## Cache Architecture

The caching system operates in memory using a multi-layered approach:

1. **Content Cache**: Stores original markdown content
2. **Rendered Cache**: Maintains pre-rendered HTML versions
3. **Compressed Cache**: Keeps gzip-compressed versions for browsers that support compression
4. **Asset Cache**: Optimized static assets like images, CSS, and JavaScript files

## How Caching Works

When a page is requested:

1. First, Waterbug checks if the page exists in the cache
2. If found, it serves the cached version immediately
3. If not found, it renders the page, caches it, and then serves it
4. If the client supports compression, the compressed version is served

## Cache Invalidation

Waterbug ensures your content stays up-to-date with:

- **Periodic Refreshes**: The cache refreshes at configurable intervals
- **File Monitoring**: Detects changes to content and theme files
- **Source Updates**: When content from git sources changes, the cache updates

## Performance Benefits

- **Reduced Rendering Time**: Pages are rendered once and reused
- **Lower CPU Usage**: Less processing needed for repeat visitors
- **Faster Response Times**: Content is served directly from memory
- **Optimized Assets**: Images and other assets are pre-optimized for delivery

The intelligent caching system allows Waterbug to handle high traffic loads efficiently while maintaining low resource consumption.

[Learn about the routing →](/About/routing)

[Back to home](/)

