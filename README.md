<h3 align="center">Hi 👋! My name is Artem and I'm a 17 y.o. ML and DS enjoyer + Self-Searcher from Khabarovsk, Russia</h3>

###

<div align="center">
</div>

###

<img align="right" height="187" src="https://i.pinimg.com/originals/ae/31/d2/ae31d2ec20c4040b1b92f7202cf26e4b.gif"  />

###

<div align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=for-the-badge" height="30" alt="python logo"  />
  <img width="12" />
  <img src="https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white&style=for-the-badge" height="30" alt="pandas logo"  />
  <img width="12" />
  <img src="https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white&style=for-the-badge" height="30" alt="numpy logo"  />
  <img width="12" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white&style=for-the-badge" height="30" alt="pytorch logo"  />
  <img width="12" />
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?logo=tensorflow&logoColor=black&style=for-the-badge" height="30" alt="tensorflow logo"  />
  <img width="12" />
  <img src="https://img.shields.io/badge/Figma-F24E1E?logo=figma&logoColor=white&style=for-the-badge" height="30" alt="figma logo"  />
  <img width="12" />
  <img src="https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black&style=for-the-badge" height="30" alt="linux logo"  />
</div>

###

<div align="center">
  <img src="https://img.shields.io/static/v1?message=Discord&logo=discord&label=&color=7289DA&logoColor=white&labelColor=&style=flat" height="40" alt="discord logo"  />
  <a href="https://t.me/gotsaweq" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Telegram&logo=telegram&label=&color=484848&logoColor=ffffff&labelColor=&style=flat" height="40" alt="telegram logo"  />
  </a>
  <a href="mailto:gotsawe@inbox.ru" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Gmail&logo=gmail&label=&color=D14836&logoColor=white&labelColor=&style=flat" height="40" alt="gmail logo"  />
  </a>
</div>

###

<br clear="both">

name: Generate snake animation

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: generate snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: dist/snake.svg?palette=github-dark


      - name: push snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
<img src="https://raw.githubusercontent.com/gotsaweq/gotsaweq/output/snake.svg" alt="Snake animation" />

###

<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=gotsaweq&radius=16&theme=react&area=true&order=5" height="300" alt="activity-graph graph"  />
</div>

###
