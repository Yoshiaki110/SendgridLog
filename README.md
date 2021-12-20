# SendgridLog

Sendgridのメール送信ログを収集する。  
（Activityログでは７日間しか保存されないため）

Herokuにデプロイ
PosgreのDBに、日時、ステータス、宛先を保存
宛先は、個人情報にあたるため、ハッシュ化（非可逆）した値で保存する

とりあえず、UIはなし、DBに直接アクセスする

# 仕様
* PATH
  * / OKのみかえす（TEXT）
  * /wh Sendgridからの呼びさき
  * /?xxx@xxx.xxx 指定のメアドのハッシュ化した値を返す（TEXT）
