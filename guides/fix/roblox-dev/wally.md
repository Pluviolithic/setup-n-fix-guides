List of issues:

1. Errors while loading shared libraries (usually libssl and libcrypto 1.1)
2. Package types not being re-exported.

List of fixes:

1.

```
wget -O /tmp/openssl.pkg.tar.zst https://archlinux.org/packages/core/x86_64/openssl-1.1/download/ 
tar --use-compress-program=unzstd -xvf /tmp/openssl.pkg.tar.zst -C /tmp
cp /tmp/usr/lib/libssl.so.1.1 /usr/lib/libssl.so.1.1
cp /tmp/usr/lib/libcrypto.so.1.1 /usr/lib/libcrypto.so.1.1
rm /tmp/openssl.pkg.tar.zst
rm -rf /tmp/usr
```
