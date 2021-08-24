## awsの流れ
- キーの作成後
 > mv コマンドを使用 →awsから作成したキーの移動
 > mv キー ~/.ssh に入れる

- chmod で使用できる権限の変更
 > sudo chmod 600 ~/.ssh/作成したキー

ssh コマンド　サーバーへのアクセス
ssh -i キーのファイル ec2-user@作成されているipアドレス

### 接続後のサーバー起動
- awsでnginxのインストール
 > sudo amazon-linux-extras install -y nginx1 
- 起動したいシステムサービス自動稼働の有効させる
 > sudo systemctl enable nginx
- 起動したいシステムサービスを起動する
 > sudo systemctl start nginx
