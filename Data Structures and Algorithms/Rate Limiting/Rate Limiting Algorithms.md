# Leaky Bucket
- Uses a queue data structure, with a limited number of requests
- Excess requests are rejected
- Requests are processed gradually overtime at a fixed rate
- Provides stable traffic control but cannot handle sudden traffic spikes
# Token Bucket
- There are a certain number of "tokens". When a request is sent, it checks for a token, if there is then the request is processed.
- Tokens are added to the bucket at a constant rate. The number of tokens in the bucket are maxed.
- Flexible for short term traffic spikes, however memory consumption may be large is there is a bucket for each user.
# Fixed Window Counter
- Divides time to specific windows, and checks there are certain requests within each window.
- System may process very high traffic at certain times (the edge times) and exceed the threshold set for each window
# Sliding Window Log
- Uses dynamic (sliding) window to count the number of requests within any given period of time.
- Window (queue data structure) removes expired times and adds new times if threshold has not been reached.
- Fine-grained traffic control, but increased complexity to manage logs
# Sliding Window Counter
Formula: `weight = (1 - proportion in current window) * lastWindowRequest + currentWindowRequest`
`proportion in current window = (time % windowLength) / windowLength`
- Above formula used to 'estimate' the weight of the next request on the server. If weight + 1 <= LIMIT, then request is processed, otherwise it is rejected.
- Serves as a balance between fixed window and sliding window.
- Intuition: the formula assumes the requests from the last window occurred at a uniform rate. Hence weights this with how far out of the previous window it is.

### Source
https://www.youtube.com/watch?v=mQCJJqUfn9Y