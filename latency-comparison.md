## Simulated Latency Results

Since access to a live CDN infrastructure was not available, the following results are simulation-based estimates created to demonstrate the expected impact of CDN edge caching.

| Region | Origin-Only Delivery | CDN-Backed Delivery | Estimated Improvement |
|--------|---------------------|---------------------|----------------------|
| India | 220 ms | 65 ms | 70% |
| Germany | 180 ms | 55 ms | 69% |

## Analysis

### India

Without a CDN, requests must travel from India to the origin server, resulting in higher network latency.

With a CDN, cached content can be served from an edge location closer to the user, reducing the estimated latency from **220 ms to 65 ms**.

### Germany

Without a CDN, users must directly access the origin server.

With CDN edge caching, the estimated latency decreases from **180 ms to 55 ms**.

## Important Note

These values are simulated estimates for project demonstration purposes. Actual latency depends on the origin location, CDN provider, network conditions, cache hit ratio, and user location.
