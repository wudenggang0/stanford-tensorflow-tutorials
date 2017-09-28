Tensorflow 同时支持Python 2.7和Python 3.3+。 <b>针对 Windows系统,  TensorFlow 仅支持64-bit Python 3.5。</b>
本课程中，我将使用Python 2.7。但是你可以使用Python 2 或者 Python 3 完成作业。开始部分的代码使用Python 2.7。

对于如何下载和安装TensorFlow，Google有详细的教程。你可以参照: https://www.tensorflow.org/get_started/os_setup

除非你的电脑有GPU，否则你应当安装没有GPU支持的TensorFlow。通常我推荐使用virtualenv安装TensorFlow。关于依赖库的清单，可以参阅requirements.txt文件。该清单会跟随课程的进度进行更新。

以下是Mac OS操作系统如何安装 tensorflow的简化版教程。如果安装TensorFlow时遇到任何问题，请在Piazza发帖：
piazza.com/stanford/winter2017/cs20si

## TensorFlow安装指南<br>
### Mac OS操作系统

在输入任何命令后遇到“permission denied”的错误时，在命令前面使用“sudo”。你将需要安装pip（如果你使用Python3,或许需要pip3）和virtualenv。

步骤 1: 安装pip和virtualenv
```bash
$ sudo easy_install pip 
$ sudo easy_install --upgrade six
$ pip install virtualenv
```

步骤 2: 创建项目目录。你将在该目录下完成所有课程。 
```bash
$ mkdir [my project]
```

步骤 3: 为项目目录设置venv virtual环境。
```bash
$ cd [my project]
$ virtualenv venv --distribute
```
这些命令将在你的项目目录下创建venv的子目录，子目录包含所有需要安装的内容 。

步骤 4: 激活venv的virtual环境 
```bash
$ source venv/bin/activate
```

如果你输入：
```bash
$ pip freeze
```

你将什么显示都看不到，这意味着在你的virtual环境中什库都没有安装。所以你必须安装你需要的所有库。本课需要的库清单，可以参阅requirements.txt文件。

步骤 5: 安装Tensorflow 及其它的依赖库
```bash
$ pip install tensorflow
$ pip freeze > requirements.txt
```

步骤 n: 
退出virtual环境，使用以下命令:
```bash
$ deactivate
```

虽然不推荐，但当你想你的virtual环境继承全局库，使用以下命令:
```bash
$ virtualenv venv --distribute --system-site-packages
```
### Ubuntu操作系统


### Windows操作系统

### 使用云
如果你不想安装TensorFlow, 你可以使用云端的TensorFlow。

#### SageMath
你可以通过云端在 https://cloud.sagemath.com/ 使用 Tensorflow。
在链接上简单点一下，创建一个账户（或者使用GitHub账户直接登陆），就可以创建TensorFlow项目。

#### Jupyter
你同样可以使用Jupyter notebook来写TensorFlow代码。

# 安装过程可能遇到的问题
## Matplotlib
在virtual环境中使用Matplotlib遇到问题时，参照以下简单的修补方式<br>
如果你使用pip安装matplotlib,在你的根目录下有一个 ~/.matplotlib 的目录。
在 ~/.matplotlib/matplotlibrc目录下创建一个文件，并增加以下代码：G: ```backend: TkAgg```

或者你可以在import matplotlib时简单的增加以下命令: ```matplotlib.use("TkAgg")```

> 以上由吴登刚翻译，如有任何问题，请联系wudenggang at outlook dot com
