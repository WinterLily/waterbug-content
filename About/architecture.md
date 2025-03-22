# 1. Architecture

Waterbug follows a modular design pattern with clearly separated concerns. The core application is built in Rust for memory efficiency and performance.

## Core Components

### Cache System
The heart of Waterbug is its memory-efficient cache that stores pre-rendered content for fast delivery. Pages are loaded, processed, and optimized once, then served from memory until content changes.

### Content Processor
Transforms markdown files into HTML using a robust markdown parser with support for GitHub-flavored markdown features.

### Dynamic Router
Maps URL paths to content files and handles complex routing scenarios.

### Theme Engine
Provides customization through themes that can be downloaded from external sources.

### Content Manager
Enables pulling content from git repositories, allowing distributed content creation.

## Runtime Flow

1. **Initialization**: Load configuration, prepare cache, initialize theme
2. **Content Loading**: Scan content directories, process markdown files
3. **Routing Setup**: Generate sitemap from content structure
4. **Server Start**: Begin serving requests from the cached content
5. **Background Tasks**: Periodically refresh content and theme sources

The modular architecture allows each component to operate independently while communicating through well-defined interfaces.

[Learn about routing →](/about/routing)

[Back to home](/)
