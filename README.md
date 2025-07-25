
这是一个基于 poetry 构建的 demo 项目，poetry 是一个现代化的 Python 依赖管理和打包工具.

**初始化新项目**

```bash
poetry new my-project
cd my-project
```

项目结构：

```
my-project/
├── .env
├── .gitignore
├── poetry.lock
├── pyproject.toml
├── README.md
├── src/
│   ├── main.py
│   └── ecoli/
│        ├── __init__.py
│        └── utils/
└── tests/
    ├── test_ecoli.py
    └── utils/
```

- 配置环境 `poetry env use python3.11`
- 安装环境 `poetry add numpy python-dotenv`，安装开发环境 `poetry add pytest --group dev`
- 兼容从 `requirement.txt` 安装，`poetry add $(cat requirements.txt)`
- 激活虚拟环境 `poetry shell`(需要安装shell引擎：`poetry self add poetry-plugin-shell`)，不激活直接运行 `poetry run python src/my_project/main.py`
- 根据目前的 .toml 调整项目的配置 [project] -> [tool.poetry]