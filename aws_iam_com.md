```
1: aws iam create-group --group-name Admins
2: aws iam list-groups

```
## awaのcliで登録する方法
- 1で上記のコマンドiamグループの作成<br>
  2で作られているグループの確認

```
1: aws iam attach-group-policy --group-name Admins --policy-arn arn:aws:iam::aws:policy/AdministratorAccess
2: aws iam list-attached-group-policies --group-name Admins
```
## ポリシーの設定
- AdministratorAccess というポリシーを Admins ユーザーグループにアタッチする
- アタッチの確認を行う


## aws configureの確認
```
aws configure list
```
上記でnoneであるとユーザーが存在してないので登録する必要がある


