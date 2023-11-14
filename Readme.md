[参考文档](https://www.jianshu.com/p/2f85142023e8) 

```bash
openssl x509 -inform PEM -subject_hash_old -in charles.pem | head -1
mv charles.pem 790a6ce6.0
mount -o remount,rw /system
adb push ./790a6ce6.0 /storage/emulated/0/Pictures
cp /storage/emulated/0/Pictures/790a6ce6.0 /system/etc/security/cacerts/
chmod 644 /system/etc/security/cacerts/790a6ce6.0

```


