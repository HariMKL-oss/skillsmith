<div align="center">
  <h1>🛠️ Skillsmith</h1>
  <p><b>Build great Claude skills — and refine them until they actually work.</b></p>
  <p>
    <a href="https://github.com/HariMKL-oss/skillsmith/stargazers"><img src="https://img.shields.io/github/stars/HariMKL-oss/skillsmith?style=for-the-badge&color=yellow" alt="Stars Badge"/></a>
    <a href="https://github.com/HariMKL-oss/skillsmith/network/members"><img src="https://img.shields.io/github/forks/HariMKL-oss/skillsmith?style=for-the-badge&color=orange" alt="Forks Badge"/></a>
    <a href="https://github.com/HariMKL-oss/skillsmith/issues"><img src="https://img.shields.io/github/issues/HariMKL-oss/skillsmith?style=for-the-badge&color=red" alt="Issues Badge"/></a>
    <a href="https://github.com/HariMKL-oss/skillsmith/blob/main/LICENSE.txt"><img src="https://img.shields.io/badge/License-Apache_2.0-blue.svg?style=for-the-badge" alt="License Badge"/></a>
  </p>
  <br>
</div>

Created and maintained by [**Hari (HariMKL-oss)**](https://github.com/HariMKL-oss).

## 🚀 What is Skillsmith?

**Skillsmith** is a powerful meta-skill: it teaches Claude how to create *other* skills. 

Point Claude at a workflow you keep repeating, and Skillsmith walks the entire Test-Driven Development (TDD) loop with you:
1. 🎯 **Capture the intent**
2. ✍️ **Draft the skill**
3. 🧪 **Run automated test cases**
4. 📊 **Review the results side-by-side**
5. 🧠 **Iteratively refine the prompt**
6. 📦 **Package it into an installable `.skill` file**

It works seamlessly in **Claude Code**, **Cowork**, and **Claude.ai**, automatically adapting its features to your environment!

---

## ✨ Features

- **Automated Benchmarking:** Measures pass-rate, execution time, and token usage for true A/B testing of your skills (Claude Code & Cowork).
- **Trigger Optimization:** Automatically generates 20 edge-case test queries and optimizes your skill description so it triggers exactly when it should.
- **Local Eval Viewer:** Spawns a local HTML UI to review test outputs and leave feedback.
- **Community Fork:** Builds upon Anthropic's open-source `skill-creator` with massive enhancements.

---

## 🛠️ Requirements

- Python 3.9+ (for packaging and evaluation scripts)
- `pyyaml` (`pip install pyyaml`)
- A Claude Code, Cowork, or Claude.ai plan that supports Custom Skills.

---

## 📥 Installation

### Option A — Install the Packaged Skill (Easiest)
1. Grab `skillsmith.skill` from the [Releases](../../releases) page (or build it yourself, below).
2. Add it to Claude:
   - **Claude.ai:** `Settings` -> `Capabilities` -> `Skills` -> Upload the `.skill` file.
   - **Claude Code:** Drop the unzipped `skillsmith/` folder into your skills directory (e.g., `~/.claude/skills/`).

### Option B — Clone and Build it Yourself
```bash
git clone https://github.com/HariMKL-oss/skillsmith.git
cd skillsmith
pip install pyyaml
python -m scripts.package_skill .
# produces skillsmith.skill in the current directory
```

---

## 🎮 Usage

Once installed, just speak to Claude naturally:

> *"Turn the way I summarize support tickets into a reusable skill."*

> *"Build me a skill that converts git commits into a changelog."*

> *"My PDF-extractor skill keeps missing tables — help me fix it."*

Skillsmith automatically figures out where you are in the process and drives from there. You don't need to memorize any steps!

---

## 📁 Repository Layout

```text
skillsmith/
├── SKILL.md          # The core skill instructions
├── scripts/          # Packaging, validation, evaluation, and trigger optimization
├── eval-viewer/      # Browser-based results UI
├── agents/           # Prompts for Grader, Comparator, and Analyzer subagents
├── references/       # JSON schemas and supporting docs
├── assets/           # UI Templates
└── LICENSE.txt       # Apache License 2.0
```

---

## 🤝 Contributing & Support

Issues and Pull Requests are incredibly welcome! If you change the behavior, please drop a note in `CHANGES.md`.

**Love Skillsmith?** Please give this repository a ⭐️ to help others discover it!

---

*Skillsmith is released under the **Apache License 2.0** (see [`LICENSE.txt`](./LICENSE.txt)). It builds on Anthropic's open-source `skill-creator` example skill; see [`NOTICE`](./NOTICE) for that attribution. This is an independent project and is not affiliated with or endorsed by Anthropic.*
