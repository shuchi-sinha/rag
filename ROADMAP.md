# Roadmap — RAG evaluation pack

One focused item per day. Each item ships with tests and a commit.
Progress is logged in [PROGRESS.md](PROGRESS.md).

This repo starts empty and grows one RAG evaluation capability at a time.
The pack is built for the questions enterprise FDE and AI roles actually ask:
is the answer grounded in retrieved documents, are citations real, and does
the agent recover when retrieval goes wrong?

## RAG pack — in order

- [ ] **Repo scaffolding** — package layout, pyproject, README, test setup, CI workflow
- [ ] **Retrieval tool + vector-store fixture** — in-memory store with documents, embeddings, and top-k retrieval
- [ ] **Poisoned-document fault** — a planted document that misleads the agent; agent should notice or fail visibly
- [ ] **Stale-embedding fault** — embeddings that no longer match their documents after an update
- [ ] **Chunk-truncation fault** — retrieved chunks cut mid-sentence; answers built on fragments
- [ ] **Groundedness evaluator** — flag answers not supported by cited retrieved documents
- [ ] **Citation-fabrication evaluator** — flag citations to documents that were never retrieved
- [ ] **Retrieval-failure-recovery evaluator** — flag agents that answer confidently when retrieval returned nothing
- [ ] **Demo scenario + docs** — one worked end-to-end example, documented in the README
- [ ] **v0.1.0 release** — version bump, release notes, changelog entry
