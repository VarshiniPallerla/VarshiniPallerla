<h1 align="center">Hi 👋, I'm Varshini Pallerla</h1>
<h3 align="center">I'm a 21-year-old software engineer and computer science enthusiast, passionate about learning and exploring new skills!</h3>

- 🔭 Student at Thapar Institute of Engineering and Technology
- 🤝 Former Intern at IIIT Hyderabad and Ernst & Young
- 💡 Fun Fact: My favorite debugging tool is… sleep 😴
- ☕ I measure caffeine in lines of code 
- 📫 Reach me through: [LinkedIn](https://www.linkedin.com/in/varshini-pallerla-311a44253/)

<h2 align="left">💼 Experience</h2>

<h3>🏢 International Institute of Information Technology (IIIT Hyderabad)</h3>
<p><strong>Summer Research Intern</strong> — Hyderabad, India</p>
<ul>
  <li>Worked on geospatial analysis and prediction of forest fire data in the Western Himalayas using Python and ArcGIS.</li>
</ul>

<h3>🏢 Ernst & Young (EY)</h3>
<p><strong>Software Developer Intern</strong> — Noida, Uttar Pradesh</p>
<ul>
  <li>Developed RESTful APIs for the UP FPO Shakti project using Spring Boot</li>
  <li>Contributed to scalable and secure backend services</li>
  <li>Focused on efficient data management and system performance optimization within a production environment</li>
</ul>

<h2 align="left">🔧 Skills</h2>

<h3 align="left">💻 Programming Languages</h3>
<p align="left">
  <a href="https://www.cprogramming.com/" target="_blank"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="C" width="40" height="40"/></a>
  <a href="https://www.w3schools.com/cpp/" target="_blank"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="C++" width="40" height="40"/></a>
  <a href="https://www.java.com" target="_blank"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="Java" width="40" height="40"/></a>
  <a href="https://www.python.org" target="_blank"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="Python" width="40" height="40"/></a>
</p>

<h3 align="left">🌐 Web Technologies</h3>
<p align="left">
  <a href="https://www.w3.org/html/" target="_blank"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="HTML5" width="40" height="40"/></a>
  <a href="https://www.w3schools.com/css/" target="_blank"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="CSS3" width="40" height="40"/></a>
</p>

<h3 align="left">🧰 Tools & Platforms</h3>
<p align="left">
  <a href="https://git-scm.com/" target="_blank"><img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="Git" width="40" height="40"/></a>
  <a href="https://postman.com" target="_blank"><img src="https://www.vectorlogo.zone/logos/getpostman/getpostman-icon.svg" alt="Postman" width="40" height="40"/></a>
  <a href="https://www.gnu.org/software/bash/" target="_blank"><img src="https://www.vectorlogo.zone/logos/gnu_bash/gnu_bash-icon.svg" alt="Bash" width="40" height="40"/></a>
</p>

<h3 align="left">🧪 Libraries and Frameworks</h3>
<p align="left">
  <a href="https://opencv.org/" target="_blank"><img src="https://www.vectorlogo.zone/logos/opencv/opencv-icon.svg" alt="OpenCV" width="40" height="40"/></a>
  <a href="https://pandas.pydata.org/" target="_blank"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/pandas/pandas-original.svg" alt="Pandas" width="40" height="40"/></a>
  <a href="https://scikit-learn.org/" target="_blank"><img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="Scikit Learn" width="40" height="40"/></a>
  <a href="https://seaborn.pydata.org/" target="_blank"><img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="Seaborn" width="40" height="40"/></a>
  <a href="https://spring.io/" target="_blank"><img src="https://www.vectorlogo.zone/logos/springio/springio-icon.svg" alt="Spring" width="40" height="40"/></a>
</p>

<h3 align="left">🗄️ Databases</h3>
<p align="left">
  <a href="https://www.mysql.com/" target="_blank"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="MySQL" width="40" height="40"/></a>
</p>


name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: platane/snk@master
        id: snake-gif
        with:
          github_user_name: VarshiniPallerla
          svg_out_path: dist/github-contribution-grid-snake.svg
      - uses: crazy-max/ghaction-github-pages@v2
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
