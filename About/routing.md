# 3. Dynamic Routing

Waterbug implements a flexible dynamic routing system that automatically creates your site structure from your content files.

## How Routing Works

1. **Content Discovery**: Waterbug scans your content directories to find markdown files
2. **Path Generation**: Creates URL paths based on file and directory structure
3. **Sitemap Building**: Builds a hierarchical representation of your site
4. **Route Matching**: Matches incoming requests against the sitemap

## Directory to URL Mapping

Waterbug translates your file structure into logical URL paths:

```
pages/
  index.md           →  /
  about.md           →  /about
  blog/
    index.md         →  /blog
    first-post.md    →  /blog/first-post
    second-post.md   →  /blog/second-post
```

## Advanced Features

- **Index Files**: Any `index.md` file represents the root of its directory
- **Title Extraction**: Automatically extracts page titles from markdown headings
- **Nested Navigation**: Automatically generates nested navigation structures
- **Client-side Navigation**: Enhances browsing with smooth transitions

The routing system also handles requests for static assets like images, CSS, and JavaScript files.

[Back to home](/)
[Understanding caching →](/about/caching)
