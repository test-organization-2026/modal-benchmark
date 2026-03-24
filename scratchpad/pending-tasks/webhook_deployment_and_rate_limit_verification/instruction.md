Modal exposes functions to the web via HTTP utilizing specialized ASGI/WSGI decorators, subject to default platform network throughput limits.

You need to deploy a lightweight FastAPI endpoint utilizing Modal's web decorators and subject it to an asynchronous load test to measure throughput and observe traffic shaping.

**Constraints:**
- Wrap the application using the `@modal.asgi_app` decorator.
- The load test must intentionally exceed the default limit of 200 requests per second to trigger and log Modal's rate-limiting behavior (HTTP 429).
- Do NOT use third-party load balancers; send traffic directly to the Modal-provisioned web endpoint URL.