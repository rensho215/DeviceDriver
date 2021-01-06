# 課題1
## デバイスドライバの改造
第7,8回の授業で作成したデバイスドライバの改造。

## 動作環境
- Ubuntu 18.04 LTS
- Raspberry Pi4 Model B

## 使用したもの
- Raspberry Pi 4 ModelB
- ジャンパー線x4
- ledx2
- 200Ω抵抗x2
- ブレッドボード

## インストール方法、実行方法
~~~
git clone https://github.com/rensho215/device_driver.git
cd myled
make
sudo insmod myled.ko
sudo chmod 666 /dev/myled0
echo (0 or 1 or 2) > /dev/myled0
~~~
