<img src="banner_github.png" alt="GitHub Banner" width="100%" />

<h1 align="center">
  <span>🐍 Watch the Snake Move Around My Name! 🐍</span>
  <br>
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=30&pause=1000&color=F7931E&width=435&lines=Hello,+I'm+Ankush+Borkar!;Data+Scientist+%7C+AI+Enthusiast+%7C+ML+Engineer;Turning+Data+Into+Insights!+📊" />
</h1>

---

## 🔥 Data Science Skills  
<p align="center">
  <img src="https://skillicons.dev/icons?i=python,sql,r,jupyter,tensorflow,pytorch,scikit-learn,pandas,numpy,matplotlib,seaborn,postgres,mongodb,sqlite,powerbi,tableau,aws,gcp,flask,fastapi" />
</p>

---

## 🐍 GitHub Contribution Snake (Moves Around My Name)  
```yaml
name: GitHub Snake Animation for Ankush Borkar

on:
  schedule:
    - cron: "0 0 * * *"  # Runs daily at midnight UTC
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    timeout-minutes: 10
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v3

      - name: Generate Snake Animation
        uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
            dist/ankush-snake.gif?color_snake=blue&color_dots=#F7931E,#FFD700,#4B0082,#9400D3

      - name: Deploy Animation to Output Branch
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./dist
          publish_branch: output
          commit_message: "🐍 Update Snake Animation [skip ci]"
