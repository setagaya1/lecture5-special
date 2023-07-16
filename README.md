# 【第５回講義＿特別課題】
__HTTPにまつわる用語について調べ、自分なりの言葉でまとめる。Markdownの記法を実践する。__
## 1. HTTPとは何か？
- ハイパーテキスト転送プロトコル (Hypertext Transfer Protocol)とは、WebサーバとWebブラウザの間で、Web情報をやりとりするためのプロトコル（通信規則）のこと。
- クライアント（Webブラウザなど）が要求を出し、サーバが応答を返す。1つの要求（リクエスト）には1つの応答（レスポンス）を返すルールになっている。
- 主な用途は上述のクライアントとサーバーのWeb情報のやり取りになるが、スマホやアプリからのサーバ機能呼び出しや、サーバ間のサービス呼び出しなどにも幅広く使われており、主に「REST API」に関係する事項で、アプリケーション開発時にプログラムが持つ機能を呼び出す場合に利用される。
## 2. HTTPとHTTPの違い
- HTTPとHTTPSの違いは通信が暗号化されていないか暗号化されているかの違いで、HTTPSが暗号化されている。
- 暗号化通信は「[SSLサーバ証明書](https://www.itmanage.co.jp/security/ssl/)」をサーバにインストールすることにより実現できる。
![image](https://github.com/setagaya1/lecture5-special/assets/136170263/d5a4f50f-b5d5-40f4-880b-58de4ce8ecfd)

## 3. URLとは何か？
- URL（Uniform Resource Locator）とは、簡単にいえばインターネット上のホームページ（Webサイト）やファイルの位置や情報を示すもの。（そのためアドレスとも呼ばれる）
- 基本的には、そのWebサイト専用住所である__ドメイン__と__ディレクトリ__、そしてそれに連なる__ファイル名__にて構成される。

## 4. クエリ文字列について調べる
### 4-1. クエリ文字列とはそもそも何か？
- クエリ文字列（URLパラメーター）とは、サーバーに情報を送るためにURLの末尾につけ足す文字列（変数）のこと。
- 「?」をURLの末尾につけ、その次に「パラメーター＝値」をつけ、複数のパラメーターをつけたい場合は「&」を使用する。  
（例：「https:// ○△×□.jp/?●=▲×■&○=△×□」）
>  参考 -そもそも「クエリ」とは？-
> - 問い合わせや質問するという意味があり、IT業界ではデータベースに対しての命令文のこと。
### 4-2. 使用用途
- __Webサイトのアクセス解析（パッシブパラメーター）__
  - パッシブパラメーターは、表示されるコンテンツに影響を及ぼさず、有無に関わらず表示されるページは同じ。
  - ユーザーがどのような経路を通って当該Webサイトへたどり着いたのかを知るために、固有のパラメーターをつけて計測できる。
  - 一般的には、集客のためにWebサイトへの流入元を分析したいときや、リスティング広告からの流入情報を知りたいときなどに使用される。
- __動的なページ結果の表示（アクティブパラメーター）__
  - アクティブパラメーターは、表示されるコンテンツに影響ぼし、記載された文字列に応じてWebサイトの表示内容を変更できる。
  - 例えばショッピングサイトの場合、アクティブパラメーターを使用することにより、商品一覧をサイズごとにフィルタリングしたり、価格順に並べ替えたりすることができる。
### 4-3. パスパラメーターとの違い
- __パスパラメーターとは何か？__
　- フロントエンドからバックエンドに値を渡すときの、値の構成要素の一つ。
  - パスパラメータでは次のようにURIのパス指定で値を渡す。{...}の部分がパスパラメータである。  
`https://hogehoge.com/category/{category_name}/...`
  - 要は、URLを構成するもののうち、ディレクトリやファイル名のことを指すものと理解（つまり一意、かぶりなしということか）
- __パスパラメーターとクエリ文字列との違いは何か？__
  - 前述のとおり、クエリ文字列はURLに追記することで+αの分析や表示ができるものであるため、__省略可__である。
  - 一方で、パスパラメーターはWebサイトを表示のためサーバーへリクエストを送る際に必要不可欠であるため__省略不可__である。
## 5. HTTPメソッドとは何か？
- Webサーバーに対してリクエストを送る際に、具体的にどのようなことを実行してほしいのかを指示する際に用いるもの。
- 代表的なものは以下のとおり。  
| HTTPメソッド | 指示内容 |
| :---: | :--- |
| GET | リソース情報を取得する。 |


