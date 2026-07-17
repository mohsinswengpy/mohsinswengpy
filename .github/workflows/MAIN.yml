name: Generate Snake Animation

on:
  schedule:
    - cron: "0 0 * * *"   # runs once a day at midnight UTC
  workflow_dispatch: {}    # lets you trigger it manually from the Actions tab
  push:
    branches:
      - main               # regenerate whenever you push to main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    steps:
      - name: Generate snake animation
        uses: Platane/snk@v3
        id: snake-gif
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
            dist/github-contribution-grid-snake-gold.gif?color_snake=gold&color_dots=#1a1b27,#3d3f63,#6c63ff,#a78bfa,#ffd93d
            dist/github-contribution-grid-snake-rainbow.gif?color_snake=%23ffffff&color_dots=#ff6b6b,#ffd93d,#6bcb77,#4d96ff,#a78bfa
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

      - name: Push snake animation to output branch
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
