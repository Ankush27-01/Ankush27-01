<img src="banner_github.png" alt="GitHub Banner" width="100%" />

<h1 align="center">
  <span>🐍 Watch the Snake Move Over My Name! 🐍</span>
  <br>
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=30&pause=1000&color=F7931E&width=435&lines=Hey+There!+I'm+Tobi+%F0%9F%91%8B;Web+Developer+%7C+Tech+Enthusiast+%F0%9F%9A%80;Building+Cool+Projects+Everyday!+%E2%9A%A1" />
</h1>

<p align="center">
  🛜 Building my own <a href="https://www.tobiasmeyhoefer.de">webpage</a> <br>
  👨🏼‍🎓 Studying Media-Based Computer Science at Berliner Hochschule für Technik <br>
  👨🏼‍💻 Web Developer since 2022 <br>
  🎬 Running my YouTube channel <i>Tobi Tackles Tech</i>  
</p>

---

## 🚀 Connect with Me  
<p align="center">
  <a href="https://www.tobiasmeyhoefer.de"><img src="https://img.shields.io/badge/Website-%23000000.svg?style=for-the-badge&logo=Google-Chrome&logoColor=white" /></a>
  <a href="https://www.youtube.com/@tobitacklestech"><img src="https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white" /></a>
  <a href="https://www.linkedin.com/in/tobiasmeyhoefer"><img src="https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:hello@tobiasmeyhoefer.de"><img src="https://img.shields.io/badge/Email-%23D14836.svg?style=for-the-badge&logo=GMail&logoColor=white" /></a>
</p>

---

## 🏆 GitHub Stats & Trophies  
<div align="center">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=tobiasmeyhoefer&show_icons=true&theme=radical&count_private=true" />
  <img height="180em" src="https://github-readme-streak-stats.herokuapp.com/?user=tobiasmeyhoefer&theme=radical" />
  <img height="180em" src="https://github-profile-trophy.vercel.app/?username=tobiasmeyhoefer&theme=dracula&column=6&margin-w=10" />
</div>

---

## 🔥 Most Used Technologies  
<div align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=tobiasmeyhoefer&theme=radical&layout=compact" />
</div>

---

## 💻 Tech Stack  
<p align="center">
  <img src="https://skillicons.dev/icons?i=ts,swift,cs,java,html,css,sass,tailwind,js,nodejs,react,redux,angular,nextjs,vite,electron,express,dotnet,graphql,powershell,nginx,mongodb,postgres,mysql,sqlite,firebase,aws,gcp,figma,adobe,vercel" />
</p>

---

## 🐍 GitHub Contribution Snake (Animated on My Name)  
```md
  # Workflow Name
  name: GitHub Snake Animation on Username

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
              dist/ocean.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9

        - name: Deploy Animation to Output Branch
          uses: peaceiris/actions-gh-pages@v3
          with:
            github_token: ${{ secrets.GITHUB_TOKEN }}
            publish_dir: ./dist
            publish_branch: output
            commit_message: "🐍 Update Snake Animation [skip ci]"
