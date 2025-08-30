# Ehsan Ghoreishi

[![Github](https://img.shields.io/github/followers/Ehsan-Ghoreishi?label=Follow&style=social)](https://github.com/Ehsan-Ghoreishi)
[![Gmail](https://img.shields.io/badge/-Gmail-c14438?style=flat&logo=Gmail&logoColor=white)](mailto:ehsan.ghoreshi62@gmail.com)

---

## 💻 About Me

Hi! I'm Ehsan Ghoreishi, a passionate programmer specializing in Python, Artificial Intelligence,Data Science, Machine Learning, JavaScript, HTML, and CSS.  
I love exploring new technologies, building intelligent solutions, and sharing knowledge with the community!

---

## 🖥 Skills

- Python
- Artificial Intelligence (AI)
- Data Science
- Machine Learning
- Deep learning
- JavaScript

---

## ⚙️ Tech Stack

![Python](https://img.shields.io/badge/-Python-05122A?style=flat-square&logo=Python&color=353535)
![JavaScript](https://img.shields.io/badge/-JavaScript-05122A?style=flat-square&logo=JavaScript&color=353535)
![HTML5](https://img.shields.io/badge/-HTML5-05122A?style=flat-square&logo=HTML5&color=353535)
![CSS3](https://img.shields.io/badge/-CSS3-05122A?style=flat-square&logo=CSS3&color=353535)
![TensorFlow](https://img.shields.io/badge/-TensorFlow-05122A?style=flat-square&logo=TensorFlow&color=353535)
![PyTorch](https://img.shields.io/badge/-PyTorch-05122A?style=flat-square&logo=PyTorch&color=353535)
![Scikit Learn](https://img.shields.io/badge/-Scikit%20Learn-05122A?style=flat-square&logo=Scikit-Learn&color=353535)
![Git](https://img.shields.io/badge/-Git-05122A?style=flat-square&logo=Git&color=353535)
![VS Code](https://img.shields.io/badge/-Visual%20Studio%20Code-05122A?style=flat-square&logo=Visual-Studio-Code&color=353535)

---

## 📫 How to reach me

Feel free to email me: [ehsan.ghoreshi62@gmail.com](mailto:ehsan.ghoreshi62@gmail.com)

name: generate animation

on:
  # run automatically every 24 hours
  schedule:
    - cron: "0 */24 * * *" 
  
  # allows to manually run the job at any time
  workflow_dispatch:
  
  # run on every push on the master branch
  push:
    branches:
    - master
    
  

jobs:
  generate:
    permissions: 
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5
    
    steps:
      # generates a snake game from a github user (<github_user_name>) contributions graph, output a svg animation at <svg_out_path>
      - name: generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
          
          
      # push the content of <build_dir> to a branch
      # the content will be available at https://raw.githubusercontent.com/<github_user>/<repository>/<target_branch>/<file> , or as github page
      - name: push github-contribution-grid-snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

---

<!-- GitHub Stats Section (optional, uncomment if you want it!) -->
<!--
<div>
  <img width="45%" align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=Ehsan-Ghoreishi&show_icons=true&locale=en&layout=compact" alt="Ehsan-Ghoreishi" />
  <img width="50%"  src="https://github-readme-streak-stats.herokuapp.com/?user=Ehsan-Ghoreishi&" alt="Ehsan-Ghoreishi" />
</div>
-->


