# Awesome LLM Wiki

A curated list of implementations, templates, papers, tools, and field examples around Andrej Karpathy's LLM Wiki pattern.

LLM Wiki is a pattern for building long-lived, agent-maintained knowledge bases. Instead of only retrieving raw chunks at query time, an LLM incrementally compiles sources into durable Markdown pages, updates cross-links, tracks contradictions, and keeps the synthesis current over time.

This list focuses on resources that help people build or understand Karpathy-style LLM Wikis: source ingestion, reusable schemas, agent workflows, domain-specific projects, research foundations, and evaluation/safety tooling.

To contribute, see [CONTRIBUTING.md](CONTRIBUTING.md).

Contents: [Original Idea](#original-idea) · [Templates And Starter Kits](#templates-and-starter-kits) · [Cases](#cases) · [Papers And Research](#papers-and-research) · [Evaluation And Safety](#evaluation-and-safety)

## Original Idea

- [LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) - Andrej Karpathy's original idea file for building personal knowledge bases with LLM agents. `idea-file` `markdown` `agent-memory`

## Templates And Starter Kits

### General Templates

- [Astro-Han/karpathy-llm-wiki](https://github.com/Astro-Han/karpathy-llm-wiki) - Agent Skills-compatible workflow for Claude Code, Cursor, Codex, OpenCode, and similar coding agents. `agent-skill` `codex` `claude-code`
- [Ar9av/obsidian-wiki](https://github.com/Ar9av/obsidian-wiki) - Framework for AI agents to build and maintain an Obsidian wiki. `obsidian` `agent-workflow`
- [AgriciDaniel/claude-obsidian](https://github.com/AgriciDaniel/claude-obsidian) - Self-organizing AI second brain for Obsidian and Claude Code. `obsidian` `second-brain`
- [NicholasSpisak/second-brain](https://github.com/NicholasSpisak/second-brain) - LLM-maintained Obsidian knowledge base built around the LLM Wiki pattern. `obsidian` `template`
- [MehmetGoekce/llm-wiki](https://github.com/MehmetGoekce/llm-wiki) - Claude Code workflow for Logseq or Obsidian with a two-layer cache architecture. `logseq` `obsidian`
- [iamsashank09/llm-wiki-kit](https://github.com/iamsashank09/llm-wiki-kit) - Starter kit for persistent structured memory from PDFs, URLs, and videos. `starter-kit` `mcp`
- [lewislulu/llm-wiki-skill](https://github.com/lewislulu/llm-wiki-skill) - Agent skill for persistent Markdown wikis with example use cases such as research deep-dives, reading companions, and team knowledge bases. `agent-skill` `template`
- [tonbistudio/llm-wiki](https://github.com/tonbistudio/llm-wiki) - LLM Wiki template with example domains such as research notes, book analysis, competitive analysis, course notes, and technical docs. `template` `multi-domain`
- [Moorcheh LLM Wiki](https://github.com/moorcheh-ai/llm-wiki/blob/main/README.md) - Template and example namespace layout for research, product, competitive, and personal wikis. `template` `namespace`

### Source Ingestion

- [Docling](https://github.com/docling-project/docling) - Document conversion toolkit for preparing PDFs, DOCX, PPTX, HTML, and other formats for GenAI workflows. `pdf` `document-conversion`
- [Marker](https://github.com/datalab-to/marker) - Converts PDFs and other documents to Markdown, JSON, chunks, and HTML. `pdf-to-markdown`
- [Firecrawl](https://github.com/firecrawl/firecrawl) - Web scraping and search tool that turns websites into clean Markdown or structured data. `web` `markdown`
- [PyMuPDF4LLM](https://pymupdf.readthedocs.io/en/latest/pymupdf4llm/) - Lightweight PDF-to-Markdown extraction built around PyMuPDF. `pdf` `markdown`

## Cases

### Implementations

- [lucasastorian/llmwiki](https://github.com/lucasastorian/llmwiki) - Open-source implementation with document upload, Claude/MCP integration, and generated wiki pages. `app` `mcp` `claude`
- [nashsu/llm_wiki](https://github.com/nashsu/llm_wiki) - Cross-platform desktop application based on the LLM Wiki pattern. `desktop-app` `knowledge-base`
- [atomicstrata/llm-wiki-compiler](https://github.com/atomicstrata/llm-wiki-compiler) - Compiler that turns raw sources into an interlinked Markdown wiki. `compiler` `markdown`
- [swarmclawai/swarmvault](https://github.com/swarmclawai/swarmvault) - Local-first LLM Wiki, knowledge graph, and agent memory store. `local-first` `knowledge-graph`
- [mduongvandinh/llm-wiki](https://github.com/mduongvandinh/llm-wiki) - LLM Wiki implementation with variants for reading companion, competitive intelligence, and job search. `implementation` `variants`

### Agent Skills And Workflows

- [6eanut/llm-wiki](https://github.com/6eanut/llm-wiki) - Claude Code skill for persistent, interlinked knowledge bases. `claude-code` `skill`
- [kfchou/wiki-skills](https://github.com/kfchou/wiki-skills) - Claude Code plugin implementing a compounding Markdown wiki workflow. `claude-code` `plugin`
- [flsteven87/llm-wiki-mcp](https://github.com/flsteven87/llm-wiki-mcp) - MCP server plus Claude Code skills for persistent Markdown wikis. `mcp` `skills`
- [Electro-resonance/LLM-WIKI-MCP](https://github.com/Electro-resonance/LLM-WIKI-MCP) - Local-first Markdown knowledge system exposed through MCP tools. `mcp` `local-first`
- [Hermes LLM Wiki Skill](https://github.com/NousResearch/hermes-agent/blob/main/skills/research/llm-wiki/SKILL.md) - Hermes Agent skill for building and querying interlinked Markdown knowledge bases. `hermes` `skill`

### Domain-Specific LLM Wikis

- [skyllwt/AutoSci](https://github.com/skyllwt/AutoSci) - Wiki-centric full-lifecycle AI research platform covering paper ingestion, ideation, experiments, writing, and rebuttal workflows. `research` `scientific-discovery`
- [MetamusicX/llm-research-wiki](https://github.com/MetamusicX/llm-research-wiki) - Personal LLM-maintained research wiki adapted for philosophy, music ontology, and posthumanism. `research` `humanities`
- [Research Wiki Skill](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/research-wiki/SKILL.md) - Persistent research knowledge base for papers, ideas, experiments, claims, and relationships across a research lifecycle. `research` `agent-skill`
- [IssacW228/student-llm-wiki](https://github.com/IssacW228/student-llm-wiki) - AI-compiled knowledge base for university students, including course notes, review flows, exam prep, and cross-course connections. `education` `student-tools`
- [mikolajkozlowskiii/claude-lift](https://github.com/mikolajkozlowskiii/claude-lift) - Personal AI-maintained LLM Wiki for gym training, progress logs, PRs, body metrics, and charts. `fitness` `health-tracking`
- [allanbian1017/psychology-wiki](https://github.com/allanbian1017/psychology-wiki) - Curated LLM-maintained knowledge base focused on psychology. `psychology` `knowledge-base`
- [Thenolypus/claude-code-cv-wiki](https://github.com/Thenolypus/claude-code-cv-wiki) - Local knowledge base for managing a professional profile, generating tailored CVs, and identifying skill gaps. `career` `cv` `job-search`
- [esxr/product-wiki](https://github.com/esxr/product-wiki) - LLM Wiki-style Claude Code plugin for persistent product knowledge bases in Obsidian. `product` `obsidian`
- [junbjnnn/llm-wiki](https://github.com/junbjnnn/llm-wiki) - Product and engineering workflow examples for PRDs, API specs, postmortems, sprint planning, and operations knowledge. `product` `engineering`
- [aswin-pn/Personal-wiki-using-Gemma-4](https://github.com/aswin-pn/Personal-wiki-using-Gemma-4) - Fully local and offline personal LLM Wiki using Ollama. `local-llm` `personal-wiki`
- [helloianneo/obsidian-ai-second-brain](https://github.com/helloianneo/obsidian-ai-second-brain) - Chinese Obsidian and Claude AI personal knowledge base guide based on the LLM Wiki methodology. `pkm` `chinese` `obsidian`

### Case Studies And Discussions

- [Wiki from Code with LLM Wiki](https://github.com/balukosuri/wiki-from-code-with-llm-wiki-karpathy/blob/main/article.md) - Code-focused variant where code changes trigger documentation updates grounded in file and line citations. `codebase` `documentation`
- [balukosuri/llm-wiki-karpathy](https://github.com/balukosuri/llm-wiki-karpathy) - Implementation article describing student notes, trip planning, hobby research, health tracking, course notes, and book club use cases. `use-cases` `article`
- [Understand-Anything discussion](https://github.com/Lum1104/Understand-Anything/discussions/125) - Discussion of combining codebase knowledge graphs with LLM Wiki as long-lived project memory. `codebase` `knowledge-graph`
- [Due Diligence Agents issue](https://github.com/zoharbabin/due-diligence-agents/issues/186) - Roadmap discussion for knowledge compounding inspired by the LLM Wiki pattern. `due-diligence` `business`
- [Home Assistant filesystem MCP discussion](https://community.home-assistant.io/t/filesystem-mcp-server-expose-your-local-directory-to-claude-karpathy-llm-wiki-for-home-assistant/1005762) - Home Assistant community project exposing local directories to Claude via MCP for Karpathy-style LLM Wiki workflows. `home-assistant` `mcp`

## Papers And Research

- [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401) - Foundational RAG paper; useful contrast for explaining how LLM Wiki differs from query-time retrieval. `rag`
- [Retrieval-Augmented Generation for Large Language Models: A Survey](https://arxiv.org/abs/2312.10997) - Survey covering naive, advanced, and modular RAG. `rag` `survey`
- [MemGPT: Towards LLMs as Operating Systems](https://arxiv.org/abs/2310.08560) - Memory-tiering architecture for extending LLM context beyond a fixed window. `memory`
- [Generative Agents](https://arxiv.org/abs/2304.03442) - Agent architecture using memory, reflection, and planning. `agent-memory`
- [A Survey on the Memory Mechanism of LLM-based Agents](https://arxiv.org/abs/2404.13501) - Survey of memory design and evaluation for LLM agents. `survey` `agent-memory`
- [A-Mem: Agentic Memory for LLM Agents](https://arxiv.org/abs/2502.12110) - Agentic memory system inspired by Zettelkasten-style connected notes. `zettelkasten` `memory`
- [Lost in the Middle](https://arxiv.org/abs/2307.03172) - Evidence that long-context models may underuse information in the middle of context. `long-context`
- [RAPTOR](https://arxiv.org/abs/2401.18059) - Recursive summaries for tree-organized retrieval; relevant to wiki summarization hierarchies. `hierarchical-summary`
- [From Local to Global: A Graph RAG Approach to Query-Focused Summarization](https://arxiv.org/abs/2404.16130) - Graph-based approach for global sensemaking over private corpora. `knowledge-graph` `graphrag`
- [LOCOMO](https://arxiv.org/abs/2402.17753) - Benchmark for very long-term conversational memory. `benchmark` `long-term-memory`

## Evaluation And Safety

- [Ragas](https://docs.ragas.io/en/stable/) - Evaluation framework for LLM applications, especially RAG-style grounding and faithfulness. `evals` `rag`
- [DeepEval](https://github.com/confident-ai/deepeval) - LLM evaluation framework for agents, RAG pipelines, and chatbots. `evals`
- [TruLens](https://github.com/truera/trulens) - Tracing and evaluation framework for LLM apps, retrievers, knowledge sources, and agents. `observability`
- [Phoenix](https://github.com/Arize-ai/phoenix) - Open-source observability and evaluation tooling for LLM, RAG, and agent systems. `observability`
- [secure-llm-wiki](https://github.com/NicoBleh/secure-llm-wiki) - Security-focused LLM Wiki implementation addressing indirect prompt injection and source poisoning. `security` `prompt-injection`
