Modal's custom Rust-based container runtime lazy-loads images, enabling fast cold starts. Baseline benchmarking requires isolating the platform overhead from user code complexity to establish the absolute minimum initialization time.

You need to deploy a minimal "Hello, World!" Python function to Modal and record the execution latency for both a pure cold invocation and a warm invocation. 

**Constraints:**
- Explicitly configure the `scaledown_window` parameter to 60 seconds on the function.
- Output the raw latency difference (in milliseconds) between the cold and warm invocations to a local file.
- Do NOT include any heavy machine learning dependencies (like PyTorch or CUDA) in the image definition for this baseline.