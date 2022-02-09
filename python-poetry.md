# python-poetry

- 過慢解決方法
```toml
[[tool.poetry.source]]
name = "our-private-repo"
url = "https://our-private-repo.jfrog.io/artifactory/api/pypi/pypi-local-our-private-repo/simple"
secondary = true
```