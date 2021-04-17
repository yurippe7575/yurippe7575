### Hi there 👋

<!--
**yurippe7575/yurippe7575** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

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

<!-- リポジトリステータス -->
[![hogehoge's github stats](https://github-readme-stats.vercel.app/api?username=yurippe7575&hide=contribs&count_private=true&show_icons=true&theme=tokyonight)](https://github.com/yurippe7575/)

<!-- ソースコード統計 -->
[![Top used Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=yurippe7575&layout=compact&theme=tokyonight)](https://github.com/yurippe7575/)

name: GitHub-Profile-Summary-Cards

on:
  schedule: # execute every 24 hours
    - cron: '* */24 * * *'
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    name: generate

    steps:
      - uses: actions/checkout@v2
      - uses: vn7n24fzkq/github-profile-summary-cards@release
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          USERNAME: ${{ github.repository_owner }}
