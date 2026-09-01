# 🌍 Global Content Delivery Strategy for a Media Platform

## 📌 Project Overview

This project presents a global content delivery strategy for a media platform that delivers images and videos to users across multiple geographical regions.

The strategy uses:

- Origin storage for original media files
- A Content Delivery Network (CDN)
- Edge caching
- Environment-independent caching rules
- Cache invalidation strategies
- Latency and cost comparisons

The objective is to improve global performance, reduce latency, minimize origin load, and provide scalable media delivery.

---

## 🎯 Objectives

- Design a global content delivery architecture.
- Deliver images and videos efficiently across multiple regions.
- Use a CDN to reduce latency.
- Define edge caching rules.
- Configure origin storage and lifecycle policies.
- Compare origin-only and CDN-backed delivery.
- Compare latency across different regions.
- Analyze cost at large traffic volumes.
- Define a cache invalidation strategy.

---

## 🏗️ Architecture

```text
                 Users Worldwide
                        |
                        v
              +------------------+
              |   CDN / Edge     |
              |    Locations     |
              +------------------+
                  |          |
            Cache Hit     Cache Miss
                  |          |
                  v          v
               User    Origin Storage
                            |
                            v
                    Images and Videos
