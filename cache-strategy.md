# Edge Caching and Cache Invalidation Strategy

## Objective

This document defines the edge caching rules and cache invalidation strategy for delivering images and videos globally.

## Edge Caching Strategy

The CDN stores frequently requested content at edge locations close to users.

### Images

Images are usually static and can be cached for a longer period.

Recommended cache policy:

```text
Cache-Control: public, max-age=86400
