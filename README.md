<h1 align="center">Hi, I'm Salih 👋</h1>

<p align="center">
  <b>I build backend systems that people can actually run.</b><br>
  A Rust WebRTC server, a Rust CLI with release binaries on three platforms, and a Python package on PyPI, all built end to end.
</p>

<p align="center">
  <a href="mailto:salihyilboga98@gmail.com"><img src="https://img.shields.io/badge/Open_to-remote_backend_roles-2ea44f?style=for-the-badge" alt="Open to remote backend roles"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Rust-000000?style=flat&logo=rust&logoColor=white" alt="Rust">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white" alt="AWS">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white" alt="Docker">
</p>

---

## ⚡ In 10 seconds

- 🦀 **Wrote a WebRTC SFU and an RTMP-to-HLS ingest server in Rust**, part of an 8-service social platform.
- 📈 **Built a data cleaner that raised model accuracy by +8.14 points on average** across 15 benchmark runs and cut training time by **~49%**.
- 📦 **Ship things people can install:** release binaries for Linux, macOS and Windows, and a package on PyPI.
- 🧪 **Tested, documented and runnable by someone else**, because code nobody can run isn't finished.

---

## 🛠️ Featured work

### 🎥 [escld](https://github.com/voidstackloop/escld): real-time video calls and live streaming

A social platform with posts, follows and moderation. It also has WebRTC video calls (screen share, in-call chat, recording) and RTMP live streaming delivered as HLS.

- **Hardest part:** routing live media between callers. I wrote the **SFU (Selective Forwarding Unit) in Rust** rather than using a hosted service.
- **8 services:** React SPA, Spring Boot API, two Rust services, three background workers, and **20 AWS CDK stacks** as infrastructure code.
- **Data:** PostgreSQL, five DynamoDB single-table designs, Redis and Elasticsearch.
- Designed and tested locally. The whole system starts with one command: `docker compose up -d`.

<p align="center"><img src="https://raw.githubusercontent.com/voidstackloop/escld/main/docs/images/diagram-architecture.png" width="720" alt="escld architecture"></p>

`Rust` `Java / Spring Boot` `TypeScript / React` `WebRTC` `AWS CDK`

---

### 📊 [buffdata](https://github.com/voidstackloop/buffdata): better training data means better models

A Python CLI and SDK that validates, deduplicates, PII-redacts and LLM-scores datasets before training. It works with OpenAI, Anthropic, Gemini or a local model. For managed runs, a **Rust worker** claims jobs from the queue and supervises each run's process.

| Benchmark (40% duplicated, 10% empty rows) | Before | After |
|---|---|---|
| DBpedia-14 | 86.97% | **96.68%** |
| Emotion | 71.23% | **83.77%** |
| AG News, 100k rows | 83.39% | **89.42%** |
| Training time, AG News 100k | 80.2 s | **42.3 s** |

On already-clean data, accuracy stays within ±0.10 points, so it doesn't damage good datasets.

`Python` `Rust` `LLM APIs` `Data quality`

---

### 🔍 [formwatch](https://github.com/voidstackloop/formwatch): finds out why people give up on government forms

A Rust CLI that drives a real browser through public-service forms (permits, benefits, license renewals). It catches broken submissions, accessibility failures, unusable mobile layouts and forms that lose what you typed.

```sh
formwatch test https://city.gov/apply
formwatch report --html
```

<p align="center"><img src="https://raw.githubusercontent.com/voidstackloop/formwatch/master/docs/images/html-report.png" width="720" alt="formwatch HTML report"></p>

[v0.1.0 released](https://github.com/voidstackloop/formwatch/releases/latest) with binaries for Linux, macOS (Intel and Apple Silicon) and Windows.

`Rust` `Chromium` `Accessibility` `CLI`

---

### 🎓 [expert-mentor](https://github.com/voidstackloop/expert-mentor): turns any LLM into a real teacher

Most AI "tutor" prompts are a persona and a vibe. This one is based on learning science: retrieval practice, spaced repetition and a learner model that remembers what you've mastered between sessions. It works with Claude, ChatGPT, Gemini, Ollama and llama.cpp, and has **zero runtime dependencies**.

```sh
pipx install expert-mentor
```

[![PyPI](https://img.shields.io/pypi/v/expert-mentor.svg)](https://pypi.org/project/expert-mentor/)

`Python` `LLM` `CLI` `Published on PyPI`

---

## 🧭 How I work

I'm self-taught and learned by building real projects instead of tutorials. For every project, I:

1. **Start with the hard problem.** I pick the part most people would outsource, like media routing or dataset contamination, and build it myself.
2. **Measure it.** I don't claim a result until a benchmark or a test backs it up.
3. **Make it runnable.** One-command setup, CI, release binaries and docs, so someone else can use it without asking me.

---

<p align="center">
  <b>Hiring for a remote backend role? I'd like to hear about it.</b><br>
  📫 <a href="mailto:salihyilboga98@gmail.com">salihyilboga98@gmail.com</a>
</p>
