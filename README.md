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
            # Default light theme
            dist/github-contribution-grid-snake.svg

            # GitHub dark theme
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

            # Premium gold theme
            dist/github-contribution-grid-snake-gold.gif?color_snake=gold&color_dots=#1a1b27,#3d3f63,#6c63ff,#a78bfa,#ffd93d

            # Rainbow theme
            dist/github-contribution-grid-snake-rainbow.gif?color_snake=%23ffffff&color_dots=#ff6b6b,#ffd93d,#6bcb77,#4d96ff,#a78bfa

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
