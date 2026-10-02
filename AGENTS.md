# Repository Instructions

Before making changes, read [AI_WORKFLOW.md](AI_WORKFLOW.md) for coding rules,
[PHILOSOPHY.md](PHILOSOPHY.md) for FFI design and ownership requirements, and
[CONTRIBUTING.md](CONTRIBUTING.md) for development and validation guidance.

For FFI changes, follow the macro-first pre-flight checklist in AI_WORKFLOW.md.
Export a library-prefixed C ABI free function that delegates to
`cimpl::cimpl_free`; the Rust function is not itself an exported C ABI symbol.
Do not let panics unwind across the C ABI boundary.

When changing FFI conventions, update AI_WORKFLOW.md and PHILOSOPHY.md together
so the implementation and AI guidance remain consistent.