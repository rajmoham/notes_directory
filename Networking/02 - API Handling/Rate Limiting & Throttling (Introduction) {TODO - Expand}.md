Rate Limiting -> Limits the number of requests clients/users can make within a certain time window

Throttling -> slowing down the rate of requests, this is done through delaying them or using slower processing methods

# Rate Limiting
Rate limiting allows a certain quota of requests to be made over a certain period of time. Any further requests are instantly rejected.

Purpose: general API traffic handling, this is a good measure against Denial of Service (Dos), or even DDos (Distributed Dos) from multiple sources - depends how the rate limiting is setup. 

# Throttling
Throttling, although would provide very slow responses, would ensure the user's requests do not get rejected. This is useful when having a lot of load on the API servers. For example using an enqueue.

Purpose: when there is traffic spikes, for example seasonal offers on a commerce site
### Dynamic Throttling
Adjust delay times by real time information e.g. CPU usage, memory, Queue Length

### Adaptive Throttling
Using machine learning and heuristics to prepare for high usage and initialising throttling before high activity.

Rate Limiting Algorithms: https://www.youtube.com/watch?v=mQCJJqUfn9Y
