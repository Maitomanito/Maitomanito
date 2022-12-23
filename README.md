### Hi there 👋

Here are some ideas to get you started:

- 🔭 I’m currently working on ... freelancer
- 🌱 I’m currently learning ...Angular, Python
- 👯 I’m looking to collaborate on ...Frontend
- 🤔 I’m looking for help with ... java (backend)
- 💬 Ask me about ... Javascript y analisis de datos 
- 📫 How to reach me: ...https://www.linkedin.com/in/josemauricioromeromoreno/
- 😄 Pronouns: ...Maito 
- ⚡ Fun fact: ... mucha musika
-->![About Me](https://raw.githubusercontent.com/mauricioromero/mauricio-romero/master/bio.gif)

---
⭐️ From [Mauricio Romero](https://github.com/mauricio-romero)
name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: Maitomanito
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  
