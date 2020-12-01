#アドバンスコース　追加プログラム
### ロボットを動かす

拡張ブロックを追加します。
追加方法は、「KRC拡張ブロックの追加方法」のドキュメントを参照してください。

動くかどうか試してみましょう。

![microbit-Robot_lesson](./fig/microbit-KRC_robot_lesson.png)



```javascript
input.onButtonPressed(Button.A, function () {
    KRCmotor.FwdGo(2)
    KRCmotor.FwdRotate(2)
    KRCmotor.RevRotate(2)
    KRCmotor.StopAll(1)
    KRCmotor.RevGo(2)
})
input.onButtonPressed(Button.B, function () {
    KRCmotor.LeftTurn(2)
    KRCmotor.RightTurn(2)
    KRCmotor.LeftSpin(2)
    KRCmotor.RightSpin(2)
    KRCmotor.FwdGo(3)
    KRCmotor.RevGo(3)
})
basic.showString("OK")
basic.clearScreen()
basic.forever(function () {
	
})
```



コースをうまく移動できるように時間を調節してプログラムを組んでみてください。

---

### 音楽を鳴らす

Microbitでは音を鳴らすことができます。
Microbitに既に入っている音を鳴らしてみましょう。

端子0をイヤホンの中心に、端子GNDを外側に接続します。

![microbit-music](./fig/microbit-music.png)



```javascript
input.onButtonPressed(Button.A, function () {
    music.startMelody(music.builtInMelody(Melodies.Dadadadum), MelodyOptions.Once)
})
input.onButtonPressed(Button.B, function () {
    music.playTone(262, music.beat(BeatFraction.Whole))
    music.playTone(294, music.beat(BeatFraction.Whole))
    music.playTone(330, music.beat(BeatFraction.Whole))
})
basic.forever(function () {
	
})
```



#### KRCのボードを使う場合

出力端子の変更が必要です。「入出力端子」->「その他」->「音を鳴らす端子を・・にする」を[「最初だけ」に置いて出力端子をP2に変更してください。

![microbit-music_krc](./fig/microbit-music_krc.png)



```javascript
input.onButtonPressed(Button.A, function () {
    music.startMelody(music.builtInMelody(Melodies.Dadadadum), MelodyOptions.Once)
})
input.onButtonPressed(Button.B, function () {
    music.playTone(262, music.beat(BeatFraction.Whole))
    music.playTone(294, music.beat(BeatFraction.Whole))
    music.playTone(330, music.beat(BeatFraction.Whole))
})
pins.analogSetPitchPin(AnalogPin.P2)

```

---

#### KRCの通常のプログラムに戻す方法

microbit-krc_proto2_ext_dance_ver_1.hex
のファイルをMicrobitにドロップアンドドロップしてください。
MicrobitのLEDに「０」、「A」が表示されていれば元に戻っています。

![microbit-Robot_reset](./fig/reset.png)
