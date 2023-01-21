# MornSounds
 
# 概要
AudioClipに対し、下記の処理を施すEditor拡張です。

* 最初の無音区間を削除
* 最後の無音区間を削除
* 音量をノーマライズ

![スクリーンショット 2023-01-21 175820](https://user-images.githubusercontent.com/50489724/213864021-d9888f5f-f379-42de-b5ec-f42e13959edd.png)

## 変換前
![1](https://user-images.githubusercontent.com/50489724/213864025-8abf1124-8015-4425-9abb-8497504dd376.png)

## 変換後
![2](https://user-images.githubusercontent.com/50489724/213864027-1477992b-40c0-49ef-866a-43590d7c4f9b.png)

# 導入方法
.unitypackage を導入下さい。

# 使い方
1．上部のツールバーより、Morn / SoundProcessor を開く。

2．Input/ClipListに、変換したいAudioClipを追加する。

3．変換内容を設定する。（詳細は後述）

4．Generateボタンを押す。

5．Output/ OutputList に変換後のAudioClipが表示される。

※ファイルはデフォルト設定で Assets / MornSounds / Export フォルダに書き出されます。
  
# 設定方法
* ClipList　変換するAudioClip

* IsCutBeginningSilence　最初の無音区間を削除するかどうか
* BeginningAmplitude　有音と判定するしきい値
* BeginningOffsetSample　有音判定となったサンプル位置を、手前側へずらすオフセット値

* IsCutEndingSilence　最後の無音区間を削除するかどうか
* EndingAmplitude　有音と判定するしきい値
* EndingOffsetSample　有音判定となったサンプル位置を、後側へずらすオフセット値

* IsNormalizeAmplitude　音量を正規化するかどうか
* Normalize Amplitude　正規化後の基準となる音量

* UnderAssetsFolderName　出力先フォルダー名

* OutputList　変換後のAudioClip
