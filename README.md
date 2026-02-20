<!--
theme: gaia
class:
 - invert
headingDivider: 2
paginate: true
-->

<!--
_class:
 - lead
 - invert
-->

# Marp to Pages Template

A GitHub template for converting Marp markdown presentations into HTML, PDF, and PPTX, automatically deployed to GitHub Pages.

---

## Overview

This template repository provides a ready-to-use GitHub Actions workflow that converts Marp-formatted markdown into presentation slides and deploys them to GitHub Pages. Write your slides in markdown, push to the `main` branch, and get a hosted HTML presentation, a PDF, and a PowerPoint file automatically.

---

## Features

- Automatic conversion of Marp markdown to HTML, PDF, and PPTX
- GitHub Pages deployment on every push to `main`
- Pull request preview deployments
- Support for images and additional slide decks in a `docs/` folder
- Pre-configured Marp CLI via Docker (v3.0.2)

---

## Prerequisites

- A **GitHub** account
- Basic knowledge of **Markdown** and **Marp** syntax
- A repository created from this template

---

## Getting Started

### Installation

1. Click **Use this template** on GitHub to create a new repository.
2. Enable GitHub Pages in your repository settings (set source to `gh-pages` branch).
3. Edit this `README.md` file with your own Marp presentation content.
4. Push your changes to the `main` branch.

### Usage

- Write your presentation slides in `README.md` using Marp syntax.
- Place additional slide decks in the `docs/` folder.
- Add images to the `img/` directory for use in your slides.
- On push, the GitHub Actions workflow builds and deploys automatically.
- Access your hosted slides at `https://<username>.github.io/<repo-name>/`.

---

## Tech Stack

- **Marp CLI** - Markdown to presentation converter
- **GitHub Actions** - CI/CD pipeline for automated builds
- **GitHub Pages** - Static site hosting
- **Docker** - Containerized Marp CLI execution

---

## Resources

- [Marp Documentation](https://marp.app/)
- [Marp CLI GitHub](https://github.com/marp-team/marp-cli)
- [Original Template by ralexander-phi](https://github.com/ralexander-phi/marp-to-pages)

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
