## Sentry 钉钉机器人插件

- 发送异常信息至钉钉机器人
- 本插件可兼容 Sentry 自身限流功能
- 可通过 `docker-compose logs -f` 查看插件日志信息 (例如使用 [onpremise](https://github.com/getsentry/onpremise) 部署)

## 安装

```bash
$ pip install sentry_dingtalk_ihoey
```

## 使用

在 `项目` 的`集成(Legacy Integrations)`页面找到 `钉钉机器人` 插件启用并设置 `Access Token`

## 参照仓储

- [sentry-dingding](https://github.com/anshengme/sentry-dingding)
- [sentry-dingtalk](https://github.com/evilbs/sentry-dingtalk)

## 发布流程

### 生成包

先确保已经安装了最新版本的 `setuptools`, `wheel`, `twine`

```sh
pip install --user --upgrade setuptools wheel twine
```

生成项目包：

```sh
python setup.py sdist bdist_wheel
```

### 发布

使用 `twine` 发布：

```sh
python -m twine upload dist/*
```
