# Cost Comparison: Origin vs CDN

## Objective

This section compares the estimated cost and resource usage of delivering media content directly from origin storage versus using a CDN.

## Assumptions

For this comparison:

- 100,000 requests per day
- Approximately 3,000,000 requests per month
- Average media object size: 1 MB
- Monthly data transfer: approximately 3 TB

Actual costs may vary depending on the cloud provider, region, storage class, and CDN pricing.

## Origin-Only Delivery

In an origin-only architecture, every request reaches the origin storage or server.

### Characteristics

- All 3 million monthly requests reach the origin.
- Higher origin bandwidth usage.
- Higher load on the origin infrastructure.
- Users far from the origin may experience higher latency.

## CDN-Backed Delivery

In a CDN architecture, frequently accessed content is served from edge locations.

Assuming a cache hit ratio of 80%:

- 80% of requests are served from the CDN edge cache.
- Only 20% of requests reach the origin.
- Origin load is significantly reduced.

## Request Comparison

| Delivery Method | Requests Reaching Origin per Month |
|---|---:|
| Origin Only | 3,000,000 |
| CDN with 80% Cache Hit Ratio | 600,000 |

## Cost Considerations

| Factor | Origin Only | CDN-Backed |
|---|---|---|
| Origin bandwidth | High | Lower |
| Origin request load | High | Reduced |
| CDN transfer cost | None | Additional cost |
| Global performance | Lower | Higher |
| Scalability | Limited by origin | Highly scalable |

## Conclusion

A CDN may introduce additional delivery costs, but it significantly reduces load on the origin and improves global performance.

For a media platform with large-scale traffic, CDN-backed delivery is generally more scalable and provides a better user experience. The exact cost benefit depends on the CDN provider, cache hit ratio, media size, and regional traffic distribution.
