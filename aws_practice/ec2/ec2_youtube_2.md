## EBSについて

- EBS(Elastic BLock store)
 > EC2にアタッチして使用する外付けディスク
 > 種類に応じてIOPSが異なる
 > スナップショット(バックアップ)の取得
 > インスタンスにくっつける
 > 複数つけることも可能
 > 同じものを違うインスタンスで共有はできない
 > 同じaviilbiltyzone出ないとアタッチできない

- EBSタイプ
 > SSDタイプ
  > 読み書きの高速化情報アクセスを主にする場合
  > 凡用SSD,　　　プロビジョンIOPS SSDの2種類
  > ↑defultで使用　　↑性能を独自で設定が可能
 > HDDタイプ
　> データの大量に保存する場合
  > スループット最適化HDD, 　　　Cold HDD
  > データの書き込みの順番の違い, ↑利用頻度の低いものでしよう

### バックアップについて

- スナップショットでバックアップ
 > EBSからスナップショットを作成してS3に保管する
 > 差分のバックアップ
 > コピーの中身を前回のものから考えて保存されていく

- AMIでバックアップ
 > インスタンスにEBSに2アタッチされている複数のEBSを丸ごとバックアップを行う
 > AMIによってEBSを元に戻せる
 > AMIが起動してスナップショットを見てマッピングして探してくる
 > ブロックデバイスマッピングでスナップショットIDで参照する

 

