# Pose Analysis 0.29

## 概要

専用の iOS アプリでチーム管理者としてサインアップしログインする。<br>
チーム管理者は、iOS アプリ、或いは、 Web のダッシュボードでチームメンバーの追加や削除が可能である。<br>
チーム管理者、及び、そのメンバーは専用の iOS アプリでログインし、姿勢推定を行い、そのデータに紐づく基本データを入力してクラウドにアップロードする。<br>
この保存にはローカル環境への保存のクラウドへのアップロードが含まれるが、これらを行うには残測定可能数を消費する。<br>
この数は、毎日ログインするごとに貰えるログインギフトか、iOS アプリ内のマイページから保存チケットを購入することによって獲得できる。<br>
また、保存されたデータは、専用の Web ダッシュボードからも確認できる。<br>
このダッシュボードにログインできるのは、チーム管理者アカウントのみ。<br>
管理者はこのダッシュボードでチームのメンバーがアップロードしたデータを一括管理できる。

## 使い方

### ユーザー管理

チーム管理者一名、そのチームに紐ずくメンバー複数名という構成。

#### チーム管理者登録

iOS アプリのトップ画面で、ボタン「サインアップ」を押下すると、管理者登録画面に遷移する。<br>
<img src="./images/ios_app_login.PNG" width="300px"><br>

管理者登録画面で、所定の情報を入力して、ボタン「登録」を押下すると、管理者アカウントが仮登録される。<br>
<img src="./images/ios_app_signup.PNG" width="300px"><br>

入力したメールアドレス宛にメールが来るので、そこにあるリンクにWebブラウザからアクセスすることでユーザーを有効化できる。<br>


#### メンバー管理

iOS アプリ内でもユーザー管理ができる。<br>
ログイン後、画面下部の右側にある「マイページ」というタブを選択すると、上部に「管理」という項目があるので、そこを選択すると、ユーザー一覧画面に遷移する。<br>
<img src="./images/ios_app_mypage.PNG" width="300px"><br>
<img src="./images/ios_app_user_list.PNG" width="300px"><br>

当該画面には、チーム内の全メンバーの一覧が表示される。<br>
一覧表の各項目には、「⭐️:  {Full Name}:  {メールアドレス」というフォーマットで表示される。<br>
チームの管理者である場合は、冒頭に⭐️がつくという仕様である。<br>

一覧の中から任意のメンバーをタップすると、アラートが表示され、その中で「Delete」を選択すると、当該メンバーが削除される。<br>
<img src="./images/ios_app_delete_user.jpeg" width="300px"><br>

また、当該画面の右上にある「＋」ボタンを押下すると、新規メンバー追加画面に遷移する。<br>
<img src="./images/ios_app_add_user.PNG" width="300px"><br>

当該画面で、新規メンバーの情報を入力して、ボタン「登録」を押下すると、新規メンバーのメールアドレス宛にメールが飛ぶ。<br>
後はサインアップの時と同様に、メール本文内のURLリンクにアクセスしてユーザーを有効化すれば登録が完了となる。

#### Web ダッシュボードへのログインとメンバー追加

チーム管理者は Web ダッシュボードにログインができる。<br>
Pose Analysis Dashboard<br>
<a href="https://pose-analysis-dashboard.com">https://pose-analysis-dashboard.com</a><br>

<img src=./images/web-dashboard-login.PNG width="800px"><br>

ログイン後、トップページビューから、ボタン「User Management」を押下すると、ユーザ管理画面に遷移する。<br>

<img src="./images/web-dashboard-top.png" width="800px"><br>
<img src="./images/web-dashboard-user-management-0.png" width="800px"><br>

ボタン「Add User」を押下すると、画面下部に新規追加するユーザー情報を入力するフォームが表示されるので、<br>
そこに入力してボタン「Submit」を押下すると、対象のチームにユーザーを追加できる。<br>
<img src="./images/web-dashboard-user-management-1.png" width="800px"><br>
<img src="./images/web-dashboard-user-management-2.png" width="800px"><br>

#### iOS アプリへのメンバーログイン

管理者アカウント、或いは、メンバーアカウント情報を入力して、iOS アプリにログインができる。<br>
<img src="./images/ios_app_login.PNG" width="300px"><br>

### 測定

iOS アプリで測定した推定結果や動画をクラウド上にアップロードすることができる。<br>
測定したデータをスマホアプリに保存、及び、クラウドにアップロードする機能は有料のチケットを購入することで利用ができる。<br>
このチケットは iOS アプリ内で購入ができる。<br>
チケットは例えば 500回分などで販売され、チーム内のメンバーが測定データを保存、及び、アップロードするごとに１回分消費される。<br>
<br>
また、チーム管理者はチームのメンバーがアップロードしたデータを Web ダッシューボードから閲覧、メモ書き、及び、ダウンロードすることができる。<br>

#### iOS アプリ

##### 測定可能な残回数の表示

「マイページ」タブを選択すると、測定 > 測定可能残回数という項目がある。<br>
<img src="./images/ios_app_mypage.PNG" width="300px"><br>

測定する度に、以下のようなアラートが表示されて、保存するかを聞かれるので、そこで保存とアップロードを行うか否かを制御している。<br>
上手く測定ができなかった時は、ここで No を押下すれば、残測定回数が不要に減少することはない。<br>
<img src="./images/ios_app_measurement_finished.PNG" width="300px"><br>

##### 測定チケットのギフトと購入

毎日、その日の最初のログイン時にギフトとして保存チケットが貰える。<br>
これによって測定データを２回分保存できる。<br>
<img src="./images/ios_app_login_gift.PNG" width="300px">

「マイページ」タブを選択すると、測定 > チケット購入 という項目があり、そこに購入可能なチケットの一覧が表示される。<br>
<img src="./images/ios_app_mypage.PNG" width="300px"><br>
<img src="./images/ios_app_ticket_list.PNG" width="300px"><br>

当該画面で、購入したいチケットを選択することで購入できる。<br>

#### Web ダッシュボード

管理者アカウントでログインし、Top ページから、ボタン「View Managements」を押下すると測定一覧が表示される。<br>
<img src="./images/web-dashboard-top.png" width="800px"><br>
<img src="./images/web-dashboard-view-management-0.png" width="800px"><br>
当該画面では、チーム内の全メンバーの測定データの一覧が時系列の降順で表示される。<br>
一覧表には、各測定データごとに以下の項目が表示されている。

- Id（測定ID）
- UserId
- Full Name（ユーザー名）
- Gender(Male/Female)
- Age
- Memo（iOSアプリで測定時に入力）
- Thumbnail （サムネイル画像。動画の丁度中間時点のフレームをサムネイル化。）
- Admin Memo（Webダッシュボードで管理者が自由に入力できる）

また、上部のテキストボックスに条件を入力することで条件検索ができる。<br>
検索項目は以下の通り。

- id （測定ID）
- Full Name （ユーザー名）
- 性別（All/Male/Female）
- Age（年齢）
- Memo
- Admin memo

##### ダウンロード

測定一覧表の右端のボタン「Download」を押下すると、測定データの一式が zip 形式でダウンロードされる。<br>
解凍すると以下のデータがある。

- video.mov
  - 録画映像。顔には灰色のマスクがかけられているが、 AIによるものなので１００％ではない。
- thumbnail.jpg
  - 一覧表に表示されているサムネイル画像。基本的には不要。
  - row.csv
    - 各部位の３次元座標の時系列データ
  - loapass.csv
    - row.csv にローパスフィルタをかけたデータ
  - kalman.csv
    - row.csv にカルマンフィルタをかけたデータ
  - angles.csv
    - row.csv を元に各関節の角度を算出したデータ
  - lowpass_angles.csv
  - kalman_angles.csv

##### 分析

測定一覧表の右の方にあるボタン「Analyze」を押下すると、対象の測定の分析画面に遷移する。<br>
<img src="./images/web-dashboard-measurement-detail.gif" width="800px"><br>
分析画面では、iOS アプリの Analyze 画面と同様の機能が実装されている。<br>
以下の項目がある。<br>
- 基本情報
  - gender
  - age
  - memo
  - admin memo

- 動画プレイヤー
  - ダウンロード動画と同様に、顔には灰色のマスクがかかっている。
- 推論結果の棒人間（動画の再生位置に同期している）
- 体の各部位の座標
  - 表示項目は上部のセレクトボックスで選択
  - 動画の再生に応じて、表示フレームの位置に赤いラインが入る
- 各関節の角度
  - 表示項目は上部のセレクトボックスで選択
  - 動画の再生に応じて、表示フレームの位置に赤いラインが入る
  
### 以上
