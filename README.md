### WELCOME TO MY PAGE 👋👋👋
My name is Huy Khanh. I am a student in FPT University. I am interested in the following topics: Deep Learning in NLP and Computer Vision, ROS2.
## 📫 How to reach me: 
[![Linkedin](https://i.stack.imgur.com/gVE0j.png) LinkedIn](https://www.linkedin.com/in/hua-huy-17705a279/) [![GitHub](https://i.stack.imgur.com/tskMh.png) GitHub](https://github.com/HyUvscode)


#DevCard:
<a href="https://app.daily.dev/Khuy"><img src="https://api.daily.dev/devcards/c95f6011eb114df19aa24f1d193799a2.png?r=8jd" width="400" alt="Khanh Huy Hua's Dev Card"/></a>
<!--
**HyUvscode/HyUvscode** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

# Visit https://github.com/lowlighter/metrics#-documentation for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          # The following scopes are required:
          #  - public_access (default scope)
          # The following additional scopes may be required:
          #  - read:org      (for organization related metrics)
          #  - read:user     (for user related data)
          #  - read:packages (for some packages related data)
          #  - repo          (optional, if you want to include private repositories)
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: HyUvscode
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Saigon
