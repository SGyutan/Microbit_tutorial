# KRCTOOL拡張ブロック追加方法

あらかじめMicrosoft Storeで「make code」で検索して[make code for micro:bit]をインストールする。

KRCのドライバーのライブラリーファイルを拡張に追加する方法


１．KRC_Libraryホルダーにある「microbit-pxt-krc-motor-easy.hex」を自分のPCにコピーする。

[KRC_Library](./KRC_Library)

※このファイルをドラックアンドドロップで読み込ませないでください!


２．makecodeを立ち上げ、拡張機能を押す

![img](./fig/KRC_setup01.png)


３．拡張機能の一番下にスクロールし「ファイルを読み込む」を押す
※一番下にあります。

![img](./fig/KRC_setup02.png)

４．「参照」を押してコピーした「microbit-pxt-krc-motor-easy.hex」ファイルを指定して、つづけるを押す

![img](./fig/KRC_setup03.png)


５．KRCTOOLブロックが追加されます

![img](./fig/KRC_setup04.png)


# KRCの通常プログラムに戻す方法

microbit-KRC_robot_.hex
のファイルをMicrobitにドロップアンドドロップしてください。

MicrobitのLEDに「０」、「A」が表示されていれば元に戻っています。

※microbit-krc_proto2_ext_dance_ver_1.hexとmicrobit-KRC_robot_.hexは同じファイルです。

![microbit-Robot_reset](./fig/reset.png)

# KRCの通常プログラムでの無線操作

ロボット側のMicrobitにKRCの通常プログラムを入れ、MicrobitのLED「A」モードになっている場合、以下のプログラムをもう一つのMicrobitに入れることで無線操作できます。
microbit-krc_radio_controller.hex
のファイルを操縦側のMicrobitにドロップアンドドロップしてください。

MicrobitのLEDに「０」が表示されます。
ABボタンを両方押して無線チャンネルを選んで下さい。ロボット側も同じようにABボタンを両方押して同じ無線チャンネルにしてください。

詳しくは、[microbit基板の使い方.pdf](./KRC_library/microbit基板の使い方.pdf)を参照してください。



