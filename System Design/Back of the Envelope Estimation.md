## Back of the Envelope Estimation

### Traffic Estimation

**Estimate Daily Active Users (DAU)**
- DAU = Number of users × Percentage of users active daily
- 1 million users × 30% = 300,000 DAU
- Approximate 300,000 to the nearest power of two, which is around \(2^{19}\) (524,288).

**Estimate Requests Per Second (RPS)**
- RPS = (DAU × Average actions per user per day) / (24 hours × 3600 seconds)
- (300,000 users × 10 actions) / (24 × 3600) ≈ 3.5 RPS
- Approximate 3.5 RPS to the nearest power of two, which is 4.

**Peak Load Estimation**
- Peak RPS = Average RPS × Peak factor (e.g., 2-3x for peak times)
- 3.5 RPS × 3 = 10.5 requests per second at peak
- Approximate 10.5 to the nearest power of two, which is 16.

### Storage Estimation

**Data Generation per User**
- Data per user per day = Average data generated per action × Actions per user per day
- 50 KB per action × 10 actions = 500 KB per user per day
- Approximate 500 KB to the nearest power of two, which is 512 KB.

**Total Data Storage**
- Total data = DAU × Data per user per day × Days of storage
- 300,000 users × 500 KB × 30 days ≈ 4.5 TB
- Approximate 4.5 TB to the nearest power of two, which is 8 TB (since \(2^{43}\) bytes ≈ 8 TB).

**Data Growth Rate**
- Growth per month = DAU × Data per user per day × 30 days
- 300,000 users × 500 KB × 30 days ≈ 4.5 TB per month
- Approximate 4.5 TB to the nearest power of two, which is 8 TB.

### Bandwidth Estimation

**Bandwidth Per Request**
- Average size of response = Response size per request × Requests per second
- 100 KB per response × 10 RPS = 1 MB per second
- Approximate 1 MB to the nearest power of two, which is 1 MB (since \(2^{20}\) bytes = 1 MB).

**Total Bandwidth Usage**
- Total bandwidth = Bandwidth per second × 3600 seconds × 24 hours
- 1 MB per second × 3600 × 24 ≈ 86.4 TB per day
- Approximate 86.4 TB to the nearest power of two, which is 128 TB (since \(2^{47}\) bytes ≈ 128 TB).

### Compute Resources Estimation

**Estimate CPU and Memory Usage**
- Average CPU usage per request = CPU usage per request × Requests per second
- 0.01 CPU per request × 10 RPS = 0.1 CPU
- Approximate 0.1 CPU to the nearest power of two, which is 0.125 (or 1/8).

**Estimate Memory Usage**
- Average memory per user session = Memory per user × Peak concurrent users
- 50 MB per user × 10,000 users = 500 GB
- Approximate 500 GB to the nearest power of two, which is 512 GB.

### Database Sizing

**Estimate Read/Write Throughput**
- Read throughput = RPS × Read operations per request
- Write throughput = RPS × Write operations per request
- Read throughput = 10 RPS × 2 operations = 20 reads per second
- Write throughput = 10 RPS × 1 operation = 10 writes per second
- Approximate 20 reads per second to the nearest power of two, which is 32.

### Cache Sizing

**Cache Hit Rate**
- Cache size = Total data size × Cache hit rate
- 4.5 TB × 50% = 2.25 TB cache size
- Approximate 2.25 TB to the nearest power of two, which is 2 TB.

**Cache Eviction Policy**
- Choose an eviction policy that suits the data access patterns and cache size.

### Cost Estimation

**Compute Costs**
- Compute cost = Number of instances × Cost per instance
- 10 instances × $0.10 per hour = $1 per hour
- Approximate $1 to the nearest power of two cost range, which is $1 or $2.

**Storage Costs**
- Storage cost = Total storage × Cost per GB
- 4.5 TB × $0.02 per GB = $90 per month
- Approximate $90 to the nearest power of two cost range, which is $128.

**Bandwidth Costs**
- Bandwidth cost = Total bandwidth × Cost per GB
- 86.4 TB × $0.01 per GB = $864 per day
- Approximate $864 to the nearest power of two cost range, which is $1024.

### Powers of Two
- \(2^{10}\) = 1 Thousand = 1KB
- \(2^{20}\) = 1 Million = 1MB
- \(2^{30}\) = 1 Billion = 1GB
- \(2^{40}\) = 1 Trillion = 1TB
- \(2^{50}\) = 1 Quadrillion = 1PB
