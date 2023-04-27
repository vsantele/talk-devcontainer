---
theme: ./theme
introImage: /water.jpg
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
transition: slide-left
css: unocss
layout: intro
hideInToc: true
title: Simplifier votre workflow de développement avec les Devcontainers
---

# Simplifier votre workflow de développement avec les Devcontainers

## Introduction et découverte

---

## hideInToc: true

# De quoi vais-je parler ?

<Toc />

---
title: Moi
layout: about-me

helloMsg: "C'est moi!"
name: Victor Santelé
imageSrc: https://avatars.githubusercontent.com/u/26800140?v=4
job: Etudiant Spécialité Data Science
line1: Fan de serverless
line2: ChatGPT d'Antoine et des stagiaires
social1: "@vsantele"
social2: "vsantele.dev"
social3: "github.com/vsantele"
---

---

## layout: section

# Introduction

C'est quoi les Devcontainers ?

---

## layout: default

- Travailler dans un Container
- Séparation des outils par rapport au projet
- Portable
- Local ou distant
- Ajout facile de features
- Cross-orchestrator
- Possibilité de pre-built des images

---

# Codespaces

## Limitations

- mounts
- forwardPorts
- shutdownAction
- 