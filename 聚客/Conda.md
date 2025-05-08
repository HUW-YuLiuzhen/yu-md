ANACONDA

1. 下载地址 ：https://www.anaconda.com/download/success  

   下载选择：Miniconda Installers，进行安装

2. 运行ANACONDA

   ![image-20250326223848736](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20250326223848736.png)

3. 执行命令安装python 3.10

   conda env list

   conda create -n rag python=3.10

   ## Conda 基础使用命令

   以下是 **Conda** 的常用命令分类整理，涵盖环境管理、包管理、配置与帮助等场景，方便快速查阅：

   ---

   ### **1. 环境管理**
   | 命令                                    | 说明                                 |
   | --------------------------------------- | ------------------------------------ |
   | `conda create --name my_env python=3.9` | 创建名为 `my_env` 的 Python 3.9 环境 |
   | `conda activate my_env`                 | **激活**进入 `my_env` 环境           |
   | `conda deactivate`                      | 退出当前环境                         |
   | `conda env list` 或 `conda info --envs` | 列出所有已创建的环境                 |
   | `conda remove --name my_env --all`      | 删除整个 `my_env` 环境               |
   | `conda env export > environment.yml`    | 导出当前环境的配置到 YAML 文件       |
   | `conda env create -f environment.yml`   | 通过 YAML 文件复现环境               |
   | `conda list`                            | 查看当前环境中已安装的包             |

   ---

   ### **2. 包管理**
   | 命令                                        | 说明                          |
   | ------------------------------------------- | ----------------------------- |
   | `conda install numpy`                       | 安装 NumPy 包（自动解决依赖） |
   | `conda install numpy=1.21`                  | 安装指定版本的 NumPy          |
   | `conda update numpy`                        | 更新 NumPy 到最新版本         |
   | `conda remove numpy`                        | 卸载 NumPy                    |
   | `conda search tensorflow`                   | 搜索可用的 TensorFlow 版本    |
   | `conda list --revisions`                    | 查看环境的历史修改记录        |
   | `conda install -c conda-forge package_name` | 从 `conda-forge` 频道安装包   |

   ---

   ### **3. 配置与清理**
   | 命令                                      | 说明                           |
   | ----------------------------------------- | ------------------------------ |
   | `conda config --show`                     | 查看 Conda 所有配置项          |
   | `conda config --add channels conda-forge` | 添加下载频道（如 conda-forge） |
   | `conda clean --all`                       | 清理缓存和未使用的包           |
   | `conda update conda`                      | 更新 Conda 自身                |

   ---

   ### **4. 实用技巧**
   - **跨平台共享环境**：  
     ```bash
     conda env export --no-builds > environment.yml  # 忽略系统相关依赖
     ```
   - **克隆环境**：  
     ```bash
     conda create --name new_env --clone old_env
     ```
   - **快速安装 Jupyter 全家桶**：  
     ```bash
     conda install jupyter notebook numpy pandas matplotlib
     ```

   ---

   ### **常见问题解决**
   - **Conda 命令未找到**：  
     需将 Conda 加入系统 PATH（安装时勾选“Add to PATH”或手动配置）。
   - **下载慢**：  
     切换国内镜像源（如清华、中科大），例如：
     ```bash
     conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
     ```

   掌握这些命令后，90% 的 Conda 使用场景都能覆盖！建议收藏备用。







Conda 和 pip 都是 Python 包管理工具，但它们的用途和命令有所不同。以下是它们的对比及常用命令：

---

## **1. Conda vs. pip 的区别**
| **功能**     | **Conda**                                    | **pip**                      |
| ------------ | -------------------------------------------- | ---------------------------- |
| **包管理**   | 可管理 Python 和非 Python 包（如 R、C++ 库） | 仅管理 Python 包             |
| **环境管理** | 支持完整的虚拟环境（`conda create`）         | 依赖 `venv` 或 `virtualenv`  |
| **依赖解决** | 更严格的依赖冲突检查                         | 依赖解决较弱，可能冲突       |
| **安装来源** | Anaconda 官方仓库、conda-forge 等            | PyPI（Python Package Index） |
| **适用场景** | 数据科学、机器学习（TensorFlow、PyTorch）    | 纯 Python 项目               |

---

## **2. Conda 常用命令**
### **环境管理**
| 命令                                     | 说明                  |
| ---------------------------------------- | --------------------- |
| `conda create --name my_env python=3.10` | 创建 Python 3.10 环境 |
| `conda activate my_env`                  | 激活环境              |
| `conda deactivate`                       | 退出当前环境          |
| `conda env list`                         | 查看所有环境          |
| `conda remove --name my_env --all`       | 删除环境              |

### **包管理**
| 命令                                  | 说明                |
| ------------------------------------- | ------------------- |
| `conda install numpy`                 | 安装 NumPy          |
| `conda install -c conda-forge pandas` | 从 conda-forge 安装 |
| `conda update numpy`                  | 更新包              |
| `conda remove numpy`                  | 卸载包              |
| `conda list`                          | 查看已安装的包      |

### **其他**
| 命令                      | 说明         |
| ------------------------- | ------------ |
| `conda search tensorflow` | 搜索可用版本 |
| `conda clean --all`       | 清理缓存     |
| `conda update conda`      | 更新 Conda   |

---

## **3. pip 常用命令**
### **包管理**
| 命令                          | 说明           |
| ----------------------------- | -------------- |
| `pip install numpy`           | 安装包         |
| `pip install numpy==1.23.5`   | 安装指定版本   |
| `pip install --upgrade numpy` | 升级包         |
| `pip uninstall numpy`         | 卸载包         |
| `pip list`                    | 查看已安装的包 |
| `pip show numpy`              | 查看包信息     |

### **环境管理**
| 命令                                     | 说明                        |
| ---------------------------------------- | --------------------------- |
| `python -m venv my_env`                  | 创建虚拟环境（Python 内置） |
| `source my_env/bin/activate` (Linux/Mac) | 激活环境                    |
| `my_env\Scripts\activate` (Windows)      | 激活环境（Windows）         |
| `deactivate`                             | 退出环境                    |

### **其他**
| 命令                              | 说明           |
| --------------------------------- | -------------- |
| `pip freeze > requirements.txt`   | 导出依赖       |
| `pip install -r requirements.txt` | 从文件安装依赖 |
| `pip check`                       | 检查依赖冲突   |

---

## **4. 什么时候用 Conda？什么时候用 pip？**
- **用 Conda**：
  - 安装科学计算包（NumPy、SciPy、TensorFlow）。
  - 需要管理非 Python 依赖（如 CUDA、FFmpeg）。
  - 希望更好的环境隔离。
- **用 pip**：
  - 纯 Python 项目。
  - PyPI 独有的包（如 Django、Flask）。
  - 在 `conda env` 里用 `pip` 安装（但需小心冲突）。

---

## **5. 最佳实践**
1. **优先用 Conda** 安装核心包（如 NumPy、Pandas）。
2. **在 Conda 环境里用 pip** 安装 PyPI 独有的包：
   ```bash
   conda create -n my_env python=3.10
   conda activate my_env
   conda install numpy pandas  # Conda 安装
   pip install flask          # pip 安装
   ```
3. **避免混用**，否则可能导致依赖冲突。

---

掌握这些命令后，你可以更灵活地管理 Python 环境！ 🚀





## PyCharm 设置运行环境使用 conda

![image-20250327233115244](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20250327233115244.png)