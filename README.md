name: Generate Contribution Snake

on:
  schedule:
    - cron: "0 0 * * *"   # regenerate daily at midnight UTC
  workflow_dispatch: {}    # allow manual trigger from the Actions tab
  push:
    branches:
      - main               # regenerate whenever you push to main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    steps:
      - name: Generate snake animation (colorful premium themes)
        uses: Platane/snk@v3
        id: snake-gif
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
            dist/github-contribution-grid-snake-gold.gif?color_snake=gold&color_dots=#1a1b27,#3d3f63,#6c63ff,#a78bfa,#ffd93d
            dist/github-contribution-grid-snake-rainbow.gif?color_snake=%23ffffff&color_dots=#ff6b6b,#ffd93d,#6bcb77,#4d96ff,#a78bfa
            dist/github-contribution-grid-snake-neon.gif?color_snake=%2300f5ff&color_dots=#0d1117,#0e4429,#006d32,#26a641,#39d353
            dist/github-contribution-grid-snake-matrix.gif?color_snake=%2300ff41&color_dots=#0d0208,#003b00,#008f11,#00ff41,#00ff41
            dist/github-contribution-grid-snake-sunset.gif?color_snake=%23ff512f&color_dots=#1a1a2e,#16213e,#e94560,#ff6b6b,#ffd93d
            dist/github-contribution-grid-snake-cyberpunk.gif?color_snake=%23f637ec&color_dots=#0d0221,#240046,#5a189a,#9d4edd,#f637ec
            dist/github-contribution-grid-snake-ocean.gif?color_snake=%2300d9ff&color_dots=#03045e,#023e8a,#0077b6,#00b4d8,#90e0ef
            dist/github-contribution-grid-snake-fire.gif?color_snake=%23ffea00&color_dots=#03071e,#6a040f,#d00000,#f48c06,#ffba08
            dist/github-contribution-grid-snake-galaxy.gif?color_snake=%23e0aaff&color_dots=#10002b,#240046,#5a189a,#9d4edd,#e0aaff
            dist/github-contribution-grid-snake-pastel.gif?color_snake=%23ff9ecd&color_dots=#fff1e6,#ffd6e0,#ffb3c6,#ff8fab,#fb6f92
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

      - name: Push snake animation to output branch
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
