Modal functions can process multiple inputs simultaneously within a single container using the `@modal.concurrent` decorator, balancing throughput and queueing delays for I/O-bound tasks.

You need to implement a Python function decorated with `@modal.concurrent` that processes 500 simulated I/O-bound requests concurrently using Python's `asyncio` event loop.

**Constraints:**
- Set `max_inputs=100` and `target_inputs=80` in the concurrency decorator.
- Ensure all 500 requests complete successfully without spawning more than 7 concurrent container instances.
- Do NOT utilize GPU resources for this specific test; utilize standard CPU-bound container instances.