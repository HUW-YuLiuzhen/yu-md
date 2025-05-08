# Python-pip相关指令



# pip常用指令清单

## 安装相关

| 指令                                 | 说明                       | 示例                              |
| ------------------------------------ | -------------------------- | --------------------------------- |
| `pip install package_name`           | 安装指定的Python包         | `pip install requests`            |
| `pip install package_name==version`  | 安装指定版本的包           | `pip install django==3.2.0`       |
| `pip install --upgrade package_name` | 升级已安装的包             | `pip install --upgrade pip`       |
| `pip install -r requirements.txt`    | 从requirements文件批量安装 | `pip install -r requirements.txt` |

## 卸载相关

| 指令                         | 说明               | 示例                  |
| ---------------------------- | ------------------ | --------------------- |
| `pip uninstall package_name` | 卸载指定的Python包 | `pip uninstall flask` |

## 信息查询

| 指令                    | 说明               | 示例                  |
| ----------------------- | ------------------ | --------------------- |
| `pip list`              | 列出已安装的所有包 | `pip list`            |
| `pip show package_name` | 显示包的详细信息   | `pip show numpy`      |
| `pip list --outdated`   | 列出所有可升级的包 | `pip list --outdated` |
| `pip --version`         | 显示pip版本信息    | `pip --version`       |

## 依赖管理

| 指令                            | 说明                 | 示例                            |
| ------------------------------- | -------------------- | ------------------------------- |
| `pip freeze > requirements.txt` | 生成requirements文件 | `pip freeze > requirements.txt` |
| `pip download package_name`     | 下载包但不安装       | `pip download pandas`           |

## 配置相关

| 指令                                  | 说明         | 示例                                                         |
| ------------------------------------- | ------------ | ------------------------------------------------------------ |
| `pip config list`                     | 显示当前配置 | `pip config list`                                            |
| `pip config set global.index-url URL` | 设置镜像源   | `pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple` |
| `pip cache purge`                     | 清除下载缓存 | `pip cache purge`                                            |

## 高级用法

| 指令                                               | 说明           | 示例                                               |
| -------------------------------------------------- | -------------- | -------------------------------------------------- |
| `pip install --user package_name`                  | 用户级别安装   | `pip install --user package_name`                  |
| `pip install --ignore-installed package_name`      | 强制重新安装   | `pip install --ignore-installed package_name`      |
| `pip install git+https://github.com/user/repo.git` | 从git仓库安装  | `pip install git+https://github.com/user/repo.git` |
| `pip install --pre package_name`                   | 安装预发布版本 | `pip install --pre package_name`                   |







# pip常用指令清单

## 安装相关

| 指令                                          | 说明                               | 示例                                   |
| --------------------------------------------- | ---------------------------------- | -------------------------------------- |
| `pip install package_name`                    | 安装指定的Python包（自动安装依赖） | `pip install requests`                 |
| `pip install --no-deps package_name`          | 只安装指定包，不安装依赖           | `pip install --no-deps django`         |
| `pip install --ignore-installed package_name` | 强制重新安装并处理依赖冲突         | `pip install --ignore-installed numpy` |

## 依赖关系处理

| 指令                                                         | 说明                                                 | 示例                                                   |
| ------------------------------------------------------------ | ---------------------------------------------------- | ------------------------------------------------------ |
| `pip check`                                                  | 检查已安装包的依赖兼容性                             | `pip check`                                            |
| `pip install package_name --upgrade-strategy eager`          | 升级时尽可能升级依赖包                               | `pip install flask --upgrade-strategy eager`           |
| `pip install package_name --upgrade-strategy only-if-needed` | 仅在需要时升级依赖包（默认策略）                     | `pip install pandas --upgrade-strategy only-if-needed` |
| `pipdeptree`                                                 | 显示完整的依赖树（需先安装`pip install pipdeptree`） | `pipdeptree`                                           |
| `pip show --files package_name`                              | 查看包安装的文件和依赖                               | `pip show --files matplotlib`                          |

## 依赖冲突解决

| 指令                                                         | 说明                       | 示例                                                         |
| ------------------------------------------------------------ | -------------------------- | ------------------------------------------------------------ |
| `pip install package_name --no-deps` + `pip install dep_package==version` | 手动指定依赖版本           | `pip install torch --no-deps`<br>`pip install numpy==1.21.0` |
| `pip install --use-deprecated=legacy-resolver`               | 使用旧版依赖解析器         | `pip install --use-deprecated=legacy-resolver conflicting_packages` |
| `pip install --force-reinstall package_name`                 | 强制重新安装并重建依赖关系 | `pip install --force-reinstall tensorflow`                   |

## 环境隔离（推荐解决依赖冲突的方案）

| 指令                       | 说明                      | 示例                         |
| -------------------------- | ------------------------- | ---------------------------- |
| `python -m venv myenv`     | 创建虚拟环境（标准库）    | `python -m venv ./venv`      |
| `source venv/bin/activate` | 激活虚拟环境（Linux/Mac） | `source ./venv/bin/activate` |
| `.\venv\Scripts\activate`  | 激活虚拟环境（Windows）   | `.\venv\Scripts\activate`    |
| `pip install pipenv`       | 安装更高级的依赖管理工具  | `pip install pipenv`         |

## 其他实用指令

| 指令                                                         | 说明                 | 示例                                             |
| ------------------------------------------------------------ | -------------------- | ------------------------------------------------ |
| `pip download package_name --no-deps`                        | 仅下载主包不下载依赖 | `pip download torch --no-deps`                   |
| `pip install --target dir package_name`                      | 安装到指定目录       | `pip install --target ./lib requests`            |
| `pip install --platform manylinux1_x86_64 --only-binary=:all: package_name` | 指定平台安装二进制包 | `pip install --platform manylinux1_x86_64 numpy` |