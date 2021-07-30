# autoconf-prebuild
some old os system package manager repo's autoconf version is too old.

## how to use
```bash
curl -LO https://github.com/leleliu008/autoconf-prebuild/releases/download/2.69/autoconf-2.69-glibc-linux-x86_64.tar.gz
tar vxf autoconf-2.69-glibc-linux-x86_64.tar.gz -C /opt
export PATH=/opt/autoconf-2.69-glibc-linux-x86_64/bin:$PATH

for xx in $(grep '/root/.zpkg/install.d/autoconf' -rl '/opt/autoconf-2.69-glibc-linux-x86_64')
do
    gsed -i 's|/root/.zpkg/install.d/autoconf|/opt/autoconf-2.69-glibc-linux-x86_64|' "$xx"
done
```

**Note:** you should install `perl` and `m4` before using it.
