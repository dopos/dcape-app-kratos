# dcape-app-kratos

[![GitHub Release][1]][2] [![GitHub code size in bytes][3]]() [![GitHub license][4]][5]

[1]: https://img.shields.io/github/release/dopos/dcape-app-kratos.svg
[2]: https://github.com/dopos/dcape-app-kratos/releases
[3]: https://img.shields.io/github/languages/code-size/dopos/dcape-app-kratos.svg
[4]: https://img.shields.io/github/license/dopos/dcape-app-kratos.svg
[5]: LICENSE

[Ory Kratos](https://www.ory.sh/kratos/) application package for [dcape](https://github.com/dopos/dcape).

## Upstream

* Project: [Ory Kratos](https://www.ory.sh/kratos/)
* Docker: [kratos](https://hub.docker.com/r/oryd/kratos)

## Requirements

* linux 64bit with git, make, sed installed
* [docker](http://docker.io) with [compose plugin](https://docs.docker.com/compose/install/linux/)
* [dcape](https://github.com/dopos/dcape) v3
* VCS service like [Gitea](https://gitea.io)
* CI/CD service like [Woodpecker CI](https://woodpecker-ci.org/)

## Install

### Via CI/CD

* VCS: Fork or mirror this repo in your Git service
* CI/CD: Activate repo
* VCS: "Test delivery", config sample will be saved to config service (enfist in dcape)
* Config: Edit config vars and remove .sample from config name
* VCS: "Test delivery" again (or CI/CD: "Restart") - app will be installed and started on CI/CD host
* After that just change source and do `git push` - app will be reinstalled and restarted on CI/CD host

### Via terminal

Run commands on deploy host with [dcape](https://github.com/dopos/dcape) installed:
```bash
git clone https://github.com/dopos/dcape-app-kratos.git
cd dcape-app-kratos
make config-if
... <edit .env>
make up
```

## License

Copyright 2024 Aleksei Kovrizhkin <lekovr+dopos@gmail.com>

Licensed under the Apache License, Version 2.0 (the "[License](LICENSE)");
