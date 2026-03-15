
Content Delivery Network distributes servers geographically. They deliver content to closest users

**Benefits**:
- lowers latency
- improves availability
- handle traffic spikes

Most popular providers: Akamai, Cloudflare, Amazon CloudFront

```
User → CDN edge server → (cache hit) → response
                     ↘ (cache miss)
                        origin server
```

Key term: **edge server** -> server closest to the users

### static vs dynamic

- **Static content** - remains constant on website - HTML, JS, CSS, some images
- **Dynamic content** - personalized for given user, e.g. social media feed, streaming

## Cache mechanics

### Cache hit vs miss

- **Cache hit** → CDN serves file directly
- **Cache miss** → CDN fetches from origin

Metrics:

- **cache hit ratio**
- **origin offload**

Example discussion question:

> “How would you improve CDN cache hit rate?”

Possible answers:

- longer TTL
- better cache keys
- avoid unnecessary query parameters
- normalize headers
## use cases

- ECommerce
- Online Gaming
- Social media
- Live Streaming / Video

## potential interview questions

- How would you design an image delivery service using CDN?
- How would you invalidate cache globally?
- Why might a CDN still have high latency?
- How do you cache API responses safely?
