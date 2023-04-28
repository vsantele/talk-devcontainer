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
hideInToc: true
---

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
- layout: section
---
# Introduction

C'est quoi les Devcontainers ?

```
Un Devcontainer est un environnement de développement isolé, exécuté dans un conteneur,
qui contient tout ce dont vous avez besoin pour développer votre application.
```

---

# Remote connection

- SSH
- WSL
- Container

---
# Particularités

- Travailler dans un Container
- Séparation des outils par rapport au projet
- Portable
- Local ou distant
- Ajout facile de features
- Cross-orchestrator
- Possibilité de pre-built des images
---


# Inconvénients

- Fortement lié à VS Code
- Fortement lié à Docker
- Manipulation avec WSL2 (GPG, SSH, etc.)
- Lenteur sous Windows (peut-être réglé)
- Doit être configuré pour chaque projet avant
- Le temps de build de l'image peut être long


--- 

# Avantages

- Pas de dépendances à installer
- Possibilité de travailler à distance
- Pas de configuration à faire pour les nouveaux arrivants
- 
---

# Templates

Devcontainer déjà préconfiguré pour un langage ou un framework.

## Exemples

- Node.js
- Rust
- K8s
- Docker outside of Docker

<https://containers.dev/templates>

---

# Features

Outils que l'ont peut ajouter facilement à un Devcontainer.

## Exemples

- Azure CLI
- Homebrew
- Terraform

<https://containers.dev/features>


---

# devcontainer.json

Fichier de configuration d'un Devcontainer.


```json
{
	"name": "Azure Functions & C# - .NET 7 (Isolated)",
	"dockerComposeFile": "docker-compose.yml",
	"service": "app",
	"forwardPorts": [ 7071, 10000, 10001, 8081],
	"portsAttributes": {
		"8081": {
			"label": "CosmosDB",
			"protocol": "https"
		}
	},
	"workspaceFolder": "/workspaces/${localWorkspaceFolderBasename}",
	"customizations": {
		"vscode": {
			"extensions": [
				"ms-azuretools.vscode-azurefunctions",
				"ms-dotnettools.csharp",
				"Azurite.azurite"
			]
		}
	},
}
```
---

# Codespaces

## Limitations

- mounts
- forwardPorts
- shutdownAction
- Docker compose
