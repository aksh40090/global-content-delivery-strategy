# Latency Comparison

## Objective

This experiment compares content delivery latency for users in two different regions, with and without a Content Delivery Network (CDN).

## Test Regions

- Asia – India
- Europe – Germany

## Expected Results

| Region | Origin-Only Delivery | CDN-Backed Delivery | Improvement |
|--------|---------------------|---------------------|-------------|
| India | Higher latency | Lower latency | Significant |
| Germany | Higher latency | Lower latency | Significant |

## Why CDN Improves Latency

Without a CDN, every user request must travel directly to the origin server. Users located far from the origin experience higher network delay.

With a CDN, cached images and videos are delivered from an edge location closer to the user. This reduces the distance travelled by the request and improves response time.

## Testing Method

Latency can be tested using:

- VPN or proxy for different regions
- Browser developer tools
- Online latency-testing tools

The same media resource should be tested from both regions with and without CDN caching enabled.

## Conclusion

CDN-backed delivery provides lower latency, especially for users located far from the origin server. Edge caching improves the user experience by reducing response time and network delay.
