
# Global Content Delivery Architecture

## Overview

This project designs a global content delivery strategy for a media platform serving images and videos to users across multiple regions.

## Architecture

Users → CDN Edge Locations → Origin Storage

The CDN caches media content at edge locations closer to users. When requested content is already cached, it is delivered directly from the nearest edge location.

If the content is not available in the cache, the CDN retrieves it from the origin storage and stores it temporarily for future requests.

## Components

### 1. Users
Users access images and videos from different geographical regions.

### 2. CDN
The Content Delivery Network distributes cached content through edge locations worldwide, reducing latency and improving performance.

### 3. Origin Storage
The origin storage stores the original images and videos.

### 4. Edge Cache
Frequently requested content is stored at edge locations for faster delivery.

## Request Flow

1. A user requests an image or video.
2. The request reaches the nearest CDN edge location.
3. If the content is cached, the CDN immediately delivers it.
4. If the content is not cached, the CDN requests it from the origin storage.
5. The CDN caches the retrieved content.
6. Future users receive the content faster from the edge cache.


   ## Origin Storage Tiering and Lifecycle Policy

Origin storage keeps the original images and videos that are delivered through the CDN.

A tiered storage strategy helps reduce storage costs by moving older or less frequently accessed content to lower-cost storage classes.

### Recommended Storage Tiers

| Content Type | Storage Tier | Purpose |
|---|---|---|
| Newly uploaded media | Standard / Hot Storage | Fast access for recently uploaded content |
| Media not accessed for 30 days | Infrequent Access / Cool Storage | Lower-cost storage for less frequently used content |
| Media not accessed for 90 days | Archive / Cold Storage | Long-term storage at a lower cost |

### Lifecycle Policy

```text
Day 0   → Store new media in Standard Storage
Day 30  → Move inactive media to Cool Storage
Day 90  → Move inactive media to Archive Storage
