<!-- markdownlint-disable-next-line -->
<div align="center">

  <!-- markdownlint-disable-next-line -->
  # Chirpy Jekyll Theme

  A minimal, responsive, and feature-rich Jekyll theme for technical writing.

  [![CI](https://img.shields.io/github/actions/workflow/status/cotes2020/jekyll-theme-chirpy/ci.yml?logo=github)][ci]&nbsp;
  [![Codacy Badge](https://img.shields.io/codacy/grade/4e556876a3c54d5e8f2d2857c4f43894?logo=codacy)][codacy]&nbsp;
  [![GitHub license](https://img.shields.io/github/license/cotes2020/jekyll-theme-chirpy?color=goldenrod)][license]&nbsp;
  [![Gem Version](https://img.shields.io/gem/v/jekyll-theme-chirpy?&logo=RubyGems&logoColor=ghostwhite&label=gem&color=orange)][gem]&nbsp;
  [![Open in Dev Containers](https://img.shields.io/badge/Dev_Containers-Open-deepskyblue?logo=linuxcontainers)][open-container]

  [**Live Demo** →][demo]

  [![Devices Mockup](https://chirpy-img.netlify.app/commons/devices-mockup.png)][demo]

</div>

## Features

- Dark Theme
- Localized UI language
- Pinned Posts on Home Page
- Hierarchical Categories
- Trending Tags
- Table of Contents
- Last Modified Date
- Syntax Highlighting
- Mathematical Expressions
- Mermaid Diagrams & Flowcharts
- Dark Mode Images
- Embed Media
- Comment Systems
- Built-in Search
- Atom Feeds
- PWA
- Web Analytics
- SEO & Performance Optimization

## Documentation

To learn how to use, develop, and upgrade the project, please refer to the [Wiki][wiki].

## Contributing

Contributions (_pull requests_, _issues_, and _discussions_) are what make the open-source community such an amazing place
to learn, inspire, and create. Any contributions you make are greatly appreciated.
For details, see the "[Contributing Guidelines][contribute-guide]".

## Credits

### Contributors

Thanks to [all the contributors][contributors] involved in the development of the project!

[![all-contributors](https://contrib.rocks/image?repo=cotes2020/jekyll-theme-chirpy&columns=16)][contributors]
<sub> — Made with [contrib.rocks](https://contrib.rocks)</sub>

### Third-Party Assets

This project is built on the [Jekyll][jekyllrb] ecosystem and some [great libraries][lib], and is developed using [VS Code][vscode] as well as tools provided by [JetBrains][jetbrains] under a non-commercial open-source software license.

The avatar and favicon for the project's website are from [ClipartMAX][clipartmax].

## License

This project is published under [MIT License][license].

[gem]: https://rubygems.org/gems/jekyll-theme-chirpy
[ci]: https://github.com/cotes2020/jekyll-theme-chirpy/actions/workflows/ci.yml?query=event%3Apush+branch%3Amaster
[codacy]: https://app.codacy.com/gh/cotes2020/jekyll-theme-chirpy/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade
[license]: https://github.com/cotes2020/jekyll-theme-chirpy/blob/master/LICENSE
[open-container]: https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/cotes2020/jekyll-theme-chirpy
[jekyllrb]: https://jekyllrb.com/
[clipartmax]: https://www.clipartmax.com/middle/m2i8b1m2K9Z5m2K9_ant-clipart-childrens-ant-cute/
[demo]: https://cotes2020.github.io/chirpy-demo/
[wiki]: https://github.com/cotes2020/jekyll-theme-chirpy/wiki
[contribute-guide]: https://github.com/cotes2020/jekyll-theme-chirpy/blob/master/docs/CONTRIBUTING.md
[contributors]: https://github.com/cotes2020/jekyll-theme-chirpy/graphs/contributors
[lib]: https://github.com/cotes2020/chirpy-static-assets
[vscode]: https://code.visualstudio.com/
[jetbrains]: https://www.jetbrains.com/?from=jekyll-theme-chirpy

## setup Lokal
```bash
bash tools/init.sh
gem install bundler

bundle install

bundle exec jekyll serve
```

if error use this for venv
```bash
sudo apt install -y build-essential libssl-dev libreadline-dev zlib1g-dev git
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(rbenv init - bash)"' >> ~/.bashrc
source ~/.bashrc

git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
rbenv install 3.2.2
rbenv local 3.2.2   # khusus di folder project
ruby -v

gem install bundler
bundle install

bundle exec jekyll serve
```

cara pakai docker
```bash
docker build -t chirpy .
docker run -p 4000:4000 chirpy
```

![alt text](images/README/image.png)

## setup to github
clone repo
```bash
token="token_github_personal_access"
git clone https://aria-nf:$token@github.com/aria-nf/aria-nf.github.io.git
# git remote set-url origin https://aria-nf:$token@github.com/aria-nf/aria-nf.github.io.git
```

- enable github pages, menggunakan source github actions
  ![alt text](images/README/image-1.png)
- configure jekyll, config.yml dan commit
- jika error berarti perlu custom dulu manifest.yml di .github/workflows
- karena di templatenya ada banyak jadi kita coba ubah jadi bak dulu aja biar gak aktif
  ![alt text](images/README/image.png)
- setelah itu tambahkan file jekyll.yml di .github/workflows dan tambahkan file dari raw ini [jekyll.yml](https://raw.githubusercontent.com/aria-nf/aria-nf.github.io/refs/heads/master/.github/workflows/jekyll.yml)

- lakukan commit dan push
  ```bash
  git add .
  git commit -am update
  git push
  ```
