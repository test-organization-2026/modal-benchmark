For high-frequency, dynamic state management, `modal.Dict` provides a distributed key-value store across the cloud cluster, backed by cloudpickle serialization.

You need to benchmark the network saturation point of `modal.Dict` by asynchronously inserting 1,000 distinct Python dictionary objects and subsequently retrieving them.

**Constraints:**
- You MUST use asynchronous primitives (e.g., `put.aio()`) to flood the dictionary and maximize throughput.
- Restrict the size of each payload to exactly 5 MiB to respect the recommended limits and avoid excessive network latency.
- Calculate and output the average latency per write operation and the total completion time for the 1,000 insertions.