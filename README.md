name: 🐍 Generate GitHub Contribution Snake

on:
  # Generate every day at midnight UTC
  schedule:
    - cron: "0 0 * * *"

  # Allow manual generation from GitHub Actions
  workflow_dispatch:

  # Regenerate whenever main is updated
  push:
    branches:
      - main

permissions:
  contents: write

jobs:
  generate:
    name: 🐍 Generate Contribution Animations
    runs-on: ubuntu-latest

    steps:
      # Generate multiple premium snake themes
      - name: 🐍 Generate Snake Animations
        uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}

          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
            dist/github-contribution-grid-snake-rainbow.gif?color_snake=%23ffffff&color_dots=#ff6b6b,#ffd93d,#6bcb77,#4d96ff,#a78bfa
            dist/github-contribution-grid-snake-neon.gif?color_snake=%2300ffff&color_dots=#0d1117,#39d353,#26a641,#00b7ff,#ff2079

        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

      # Publish generated animations to output branch
      - name: 🚀 Publish Snake Animations
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist

        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
