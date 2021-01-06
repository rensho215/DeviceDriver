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
git clone https://github.com/rensho215/DeviceDriver.git
cd myled
make
sudo insmod myled.ko
sudo chmod 666 /dev/myled0
echo 2 > /dev/myled0
echo 3 > /dev/myled0
echo 1 > /dev/myled0
echo 0 > /dev/myled0
~~~

## 回路図
下の画像のように回路を作成しました。
左のledはGPIO18,GND9番のピンに、
真ん中のledはGPIO22,GND14番のピンに、
右のledはGPIO25,GND39番のピンにそれぞれ接続されています。
![IMG_5487](https://user-images.githubusercontent.com/72724172/103721117-4018d480-5010-11eb-86de-aabe04daed3f.JPG)

## 改造事項
- echo 0 の時はすべてのledが消灯。
- echo 1 の時はすべてのledが点灯。
- echo 2 の時は左のledと真ん中のledが点灯。
- echo 3の時は真ん中のledと右のledが点灯。

## 動画
動画のurl:
