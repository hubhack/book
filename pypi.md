包管理

setuptools

包结构

```python
#from distutils.core import setup
from setuptools import setup
# 导入setup函数并传参
setup(
    name = '',
    version= '0.0.1',
    author = 'mwq',
    author_email = '',
    packages = ['',], 
)
```

buile命令, 编译

python setup.py build

build后就可以install, 直接运行

python setup.py install

如果没有build, 会先build编译, 然后安装



sdist命令

>  python setup.py sdist

创建源代码的分发包

产生一个dist目录,里面生成一个带版本号的压缩包

在其他地方解压缩这个文件,里面有setup.py, 就可以使用python setup.py install安装了,也可以 pip install 直接使用功能pip安装这个压缩包

bdist命令

二进制分发包, 或称为安装程序, 他可以生成目标系统的安装程序

```pytohn
制作windows下的安装包
python setup.py bdist_wininst
python setup.py bdist_msi
python setup.py bdist --format=msi
rpm包
python setup.py bdist_rpm
python setup.py bdist --format=rpm
压缩文件
python setup.py bdist --format=zip
python setup.py bdist --format=gztar

```

wheel包

pip install wheel 包

做好之后 可以上传到pypi上, 

下载twine

twine upload dist/*

即可上传到pypi

