🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

<div align="center">

# 🎲 Soc Ops

### Social Bingo for In-Person Mixers

**Find people who match the prompts. Get 5 in a row. Win the crowd.**

[![Live Demo](https://img.shields.io/badge/🎮_Live_Demo-Play_Now-4f46e5?style=for-the-badge)](https://copilot-dev-days.github.io/agent-lab-java/)
[![Lab Guide](https://img.shields.io/badge/📚_Lab_Guide-Start_Here-16a34a?style=for-the-badge)](workshop/GUIDE.md)
[![Java 21](https://img.shields.io/badge/Java-21-f59e0b?style=for-the-badge&logo=openjdk)](https://adoptium.net/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.4-6db33f?style=for-the-badge&logo=spring)](https://spring.io/projects/spring-boot)

</div>

---

## ✨ What Is Soc Ops?

Soc Ops is a **hands-on GitHub Copilot workshop** wrapped inside a real, working app. You start with a simple Social Bingo game and use **VS Code Agent Mode** to redesign, extend, and ship features — experiencing the full agentic development loop from context engineering to multi-agent TDD.

> 💡 It's not just a demo. You'll build something you're proud of by the end.

---

## 🚀 What You'll Build & Learn

| # | Skill | What Happens |
|---|-------|--------------|
| 🧠 | **Context Engineering** | Teach Copilot your codebase with workspace instructions |
| 🎨 | **Design-First Frontend** | Redesign the entire UI — your theme, your vision |
| 🎭 | **Custom Agents** | Create a Quiz Master agent that writes your icebreakers |
| 🧪 | **Multi-Agent TDD** | Ship new game features with Red → Green → Refactor agents |

---

## 📚 Lab Guide

| Part | Title | Time |
|------|-------|------|
| [**00**](workshop/00-overview.md) | Overview & Checklist | — |
| [**01**](workshop/01-setup.md) | Setup & Context Engineering | 15 min |
| [**02**](workshop/02-design.md) | Design-First Frontend | 15 min |
| [**03**](workshop/03-quiz-master.md) | Custom Quiz Master | 10 min |
| [**04**](workshop/04-multi-agent.md) | Multi-Agent Development | 20 min |

> ⏱ **Total:** ~1 hour &nbsp;|&nbsp; 🎯 **Level:** Intermediate &nbsp;|&nbsp; ☕ **Stack:** Java 21 / Spring Boot / Maven

---

## ⚡ Quick Start

**Prerequisites:** [Java 21 JDK](https://adoptium.net/) · [Maven 3.9+](https://maven.apache.org/) · VS Code v1.107+ · GitHub Copilot

```bash
# Clone and run
cd socops
./mvnw spring-boot:run
```

Then open [http://localhost:8080](http://localhost:8080) — your bingo board is live.

```bash
# Build & test
./mvnw clean package
./mvnw test
```

> 🐳 **Prefer containers?** Open in the included DevContainer for a zero-setup environment.

---

## 🌍 Translations

This lab guide is available in multiple languages:

- 🇧🇷 [Português (BR)](README.pt_BR.md)
- 🇪🇸 [Español](README.es.md)

---

<div align="center">

Deploys automatically to **GitHub Pages** on push to `main`.

Made with ☕ and 🤖 for GitHub Copilot Dev Days.

</div>
