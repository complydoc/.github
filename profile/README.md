Offline document analysis for LLM pipelines.

Core library:

- [`complydoc`](https://github.com/complydoc/complydoc) – command line tool and Python library that reports on documents before they enter an LLM pipeline: token cost across models and extraction paths, extraction readiness, personal and financial identifiers (masked), and hidden or instruction-like content. Runs locally, with outbound network access blocked.

Loader and pipeline tooling, in the same package:

- `inspect_documents` and `compare_loaders` – what LangChain and LlamaIndex loaders extract, the metadata they attach and the connections they attempt, compared side by side with expected facts
- `inspect_chunks` and `complydoc chunks` – chunk sizes, sentences and tables cut at a boundary, identifiers repeated across chunks
- `MaskIdentifiers`, `DropHiddenPassages`, `StripPathMetadata` – pipeline steps for LangChain and LlamaIndex documents
- `diff_reports`, `expect` and `complydoc diff` – baselines and assertions for tests and CI

Examples:

- [`playground`](https://github.com/complydoc/playground) – runnable command line and Python examples on sample documents, with a CI workflow that fails when a report regresses against a baseline

Learn more:

- [Documentation](https://complydoc.github.io/complydoc/) – guides, command line and Python API reference, report JSON schema [(source)](https://github.com/complydoc/complydoc/tree/main/docs)
- [PyPI](https://pypi.org/project/complydoc/) – `uv tool install complydoc` or `pip install complydoc`
- [Changelog](https://github.com/complydoc/complydoc/blob/main/src/complydoc/CHANGELOG.md)
- [Issues](https://github.com/complydoc/complydoc/issues) – bug reports and feature requests
