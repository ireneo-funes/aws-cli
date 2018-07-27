# Install the AWS CLI in a Virtual Environment

The first step is to install the [virtualenv](https://virtualenv.pypa.io/) software package.

```console
❯ pip3 install virtualenv
Collecting virtualenv
  Downloading https://files.pythonhosted.org/packages/b6/30/96a02b2287098b23b875bc8c2f58071c35d2efe84f747b64d523721dc2b5/virtualenv-16.0.0-py2.py3-none-any.whl (1.9MB)
    100% |████████████████████████████████| 1.9MB 6.8MB/s
Installing collected packages: virtualenv
Successfully installed virtualenv-16.0.0
```

```console
~/Desktop
❯ python3 -m virtualenv AWS
Using base prefix '/Library/Frameworks/Python.framework/Versions/3.7'
/Library/Frameworks/Python.framework/Versions/3.7/lib/python3.7/site-packages/virtualenv.py:1041: DeprecationWarning: the imp module is deprecated in favour of importlib; see the module's documentation for alternative uses
  import imp
New python executable in /Users/ytyoun/Desktop/AWS/bin/python3
Also creating executable in /Users/ytyoun/Desktop/AWS/bin/python
Installing setuptools, pip, wheel...done.

~/Desktop
❯ cd AWS

~/Desktop/AWS
❯ ls
bin                include            lib                pip-selfcheck.json
```

```console
~/Desktop/AWS
❯ source bin/activate

~/Desktop/AWS
(AWS) ❯ pip list
Package    Version
---------- -------
pip        18.0
setuptools 40.0.0
wheel      0.31.1

~/Desktop/AWS
(AWS) ❯ pip install awscli -U
Collecting awscli
  Downloading https://files.pythonhosted.org/packages/18/6e/0cc7c4b919c848674f1513c9ac7670638a0b9fc275df226578c6f12e212b/awscli-1.15.66-py2.py3-none-any.whl (1.3MB)
    100% |████████████████████████████████| 1.3MB 3.2MB/s
Collecting colorama<=0.3.9,>=0.2.5 (from awscli)
  Using cached https://files.pythonhosted.org/packages/db/c8/7dcf9dbcb22429512708fe3a547f8b6101c0d02137acbd892505aee57adf/colorama-0.3.9-py2.py3-none-any.whl
Collecting PyYAML<=3.13,>=3.10 (from awscli)
  Using cached https://files.pythonhosted.org/packages/9e/a3/1d13970c3f36777c583f136c136f804d70f500168edc1edea6daa7200769/PyYAML-3.13.tar.gz
Collecting s3transfer<0.2.0,>=0.1.12 (from awscli)
  Downloading https://files.pythonhosted.org/packages/d7/14/2a0004d487464d120c9fb85313a75cd3d71a7506955be458eebfe19a6b1d/s3transfer-0.1.13-py2.py3-none-any.whl (59kB)
    100% |████████████████████████████████| 61kB 9.1MB/s
```

```console
~/Desktop/AWS   27s
(AWS) ❯ pip list
Package         Version
--------------- -------
awscli          1.15.66
botocore        1.10.65
colorama        0.3.9
docutils        0.14
jmespath        0.9.3
pip             18.0
pyasn1          0.4.4
python-dateutil 2.7.3
PyYAML          3.13
rsa             3.4.2
s3transfer      0.1.13
setuptools      40.0.0
six             1.11.0
wheel           0.31.1
```

## Updating AWS CLI

Once AWS CLI is installed in a virtual environment,
you can easily check which packages need to be updated.

```console
~/Desktop/AWS
(AWS) ❯ pip list --outdated
Package         Version Latest  Type
--------------- ------- ------- -----
astroid         1.6.3   1.6.5   wheel
attrs           17.4.0  18.1.0  wheel
awscli          1.15.45 1.15.56 sdist
boto3           1.7.28  1.7.55  wheel
botocore        1.10.45 1.10.55 wheel
chalice         1.3.0   1.5.0   wheel
click           6.6     6.7     wheel
colorama        0.3.7   0.3.9   wheel
idna            2.6     2.7     wheel
pyasn1          0.4.2   0.4.3   wheel
pylint          1.8.4   1.9.2   wheel
python-dateutil 2.6.1   2.7.3   wheel
PyYAML          3.12    3.13    sdist
requests        2.18.4  2.19.1  wheel
setuptools      39.0.1  40.0.0  wheel
urllib3         1.22    1.23    wheel
wheel           0.31.0  0.31.1  wheel
```

Updating a package needs an option `--upgrade`, which can be abbreviated to `-U`.

```console
~/Desktop/AWS   7s
(AWS) ❯ pip install awscli -U
```
