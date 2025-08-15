 # Caching

- GET requests are cacheable to improve performance:
  - Animals list and individual animal data cached for 5 minutes
  - FeedingSchedules list cached for 5 minutes
- POST, PUT, DELETE invalidate related caches immediately
- Cache-Control headers:
  - For GET responses: `Cache-Control: public, max-age=300`
- Reasons for caching:
  - Improve response time and reduce server load
- Methods not cached:
  - All write operations (POST, PUT, DELETE) to avoid stale data
