# Install the AWS CLI in a Virtual Environment

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
