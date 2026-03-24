Modal Sandbox environments allow dynamic, interactive, and isolated execution of unverified code, serving as the foundational infrastructure for "Code Interpreter" style AI agents.

You need to programmatically spawn an ephemeral Linux environment using `modal.Sandbox.create()`, execute a custom Bash script that computes a mathematical sequence, and securely capture the output.

**Constraints:**
- The execution must occur entirely within the Sandbox, isolated from the primary Modal app container.
- You must programmatically await the completion of the Sandbox process and stream `stdout` to the local terminal.
- Ensure the Sandbox process is configured to automatically terminate upon script completion to prevent billing leaks.