---
title: Hugoを使用して個人的なブログを作成する方法
slug: How to build a personal blog with Hugo
description: この記事では、Hugoを使用して個人的なブログや予防策を作成する方法を紹介します
date: 2023-04-20T21:50:24+08:00
image: cover.webp
categories: ["テクノロジー"]
tags: ["ブログ", "ヒューゴ"]
keywords: ["ブログ", "ヒューゴ"]
toc: true
コメント：真
読書タイム：本当
---
> 警告: この記事は機械翻訳されているため、品質が低かったり不正確な情報が含まれる可能性があります。よくお読みください。
## 序文

最近、私はインターンシップに参加しました。1つはスケジュールを調整することであり、もう1つは仕事に適応することです。3つ目は、学習と処理を必要とするコース関連のコンテンツがあることです。今日のスケジュールはついにほぼ調整されます。宿題を処理した後、ブログを書くのに忙しいです。

このトピックを書く理由も非常に簡単です。私は2日前にブログを作成し、いくつかの経験を書いて、皆と共有するためにピットに足を踏み入れました。同様に、多くの人々がすでに同様のトピックを書いているので、私は機械的に繰り返すことなくリンクを直接貼り付けます。私はそれで使用した知識を整理します。

## 参照リンク

1。[Webサイトを構築するための世界のファセストフレームワーク| Hugo（gohugo.io）](https://gohugo.io)
2。[無料の個人ブログシステムの構築および展開ソリューション（Hugo + Github Pays + Cusdis）・Pseudoyu](https://www.pseudoyu.com/zh/2022/03/24/free_blog_deploy_using_hugo_and_cusdis)
3 ..[Hugo + Githubアクション、あなたのブログ自動リリースシステムを構築・Pseudoyu](https://www.pseudoyu.com/zh/2022/05/29/deploy_your_blog_using_hugo_and_github_action)
4 ..[軽量のオープンソース無料ブログレビューシステムソリューション（Cusdis +鉄道）・Pseudoyu](https://www.pseudoyu.com/zh/2022/05/24/free_and_lightweight_blog_comment_system_using_cusdis_and_railway)
5。[無料の個人的なブログデータ統計システム（UMAMI + Vercel + Heroku）を確立してください。Pseudoyu](https://www.pseudoyu.com/zh/2022/05/21/free_blog_analysis_using_umami_vercel_and_heroku)
6。[個人のウェブサイトの確立プロセス（1）：個人ドメイン名を購入し、動的ドメイン名分析を構成（jinli.cyou）](https://jinli.cyou/p/个人网站的建立过程一购买个人域名并配置动态域名解析)
7。[個人のウェブサイトの確立（2）：Hugo Frameworkを使用して個人のWebサイトを構築する（jinli.cyou）](https://jinli.cyou/p/个人网站的建立过程二使用hugo框架搭建个人网站)
8。[個人Webサイトの確立プロセス（3）：Hugoテーマスタックの使用と最適化（jinli.cyou）](https://jinli.cyou/p/个人网站的建立过程三hugo主题stack的使用与优化/#语言转换按)
9。[個人ウェブサイトの確立プロセス（4）：サイト検索エンジン最適化（SEO）（jinli.cyou）](https://jinli.cyou/p/个人网站的建立过程四网站的搜索引擎优化seo)

## ヒューゴとは何ですか？

### 静的ページジェネレーター

実際、個人的なブログを作成したい場合は、上記のリンクを見るだけで十分です。しかし、私はまだ必要な手順を簡単に紹介します。 Hugoは静的なページジェネレーターです。マークダウンテキストの学生と選択したテーマに基づいて、美しい静的ページを生成できます。静的ページの利点は、展開が比較的便利で、応答速度が高速であり、不利な点が明らかであることです。ページをリアルタイムで編集することはできません。ページデプロイをサーバーに編集する必要があります（もちろん絶対的ではありません。 ）、そしていくつかの伝統的な伝統を統合することは困難です。フロントとバックのダイナミックページの機能。それでも、静的ページ、またはHugoは個人に十分です。

### Hugoのインストールと使用

この部分は非常にシンプルです。公式ウェブサイトで直接それを行うだけです[クイックスタート| Hugo（gohugo.io）](https://gohugo.io/getting-started/quick-start)公式ウェブサイトには、Hugoをダウンロードし、テーマの設定、投稿の投稿を行うための重要な手順があります。非常に簡単なチュートリアルが提供されています。

**ピット1 **：「Wing Install Hugo.hugo.extended」を使用してWindowsプラットフォームでHugoをダウンロードする場合、Hugo.exeをブログフォルダーにHugoインストールディレクトリにコピーする必要がある場合インストールディレクトリ。内部では、 `./hugo.exe server -d`などの相対パスの形でHugo関連の命令を実行して、通常実行できます。

### ヒューゴのテーマの選択とインストール

到着できます[完全なリスト|ヒューゴテーマ（gohugo.io）](https://themes.gohugo.io)お気に入りのテーマを閲覧します。テーマを使用する場合は、詳細ページのデモをクリックしてオンラインの例を表示できます（一部のテーマにはデモがありません）。GithubWarehouse、これはこのテーマの詳細情報に関するものです）。 「git clone links posity」またはgit submodule addls positon`を使用して、テーマをブログディレクトリにクローン化します。EmplesiteSubfolderでは、フォルダーを使用して高速展開に使用できます（以前の構成ファイルを保存することに注意してください）。テーマがテーマの公式ウェブサイトの例とは大きく異なると思われる場合は、確率が問題です。現時点では、ディレクトリ名、ファイル名、ファイルヘッダー情報などを確認する必要があります。

![ヒューゴのスタックテーマ](image-20230420222917912.png)
## 「Github Action」を使用して、ブログを自動的にリリースします

もちろん、自動リリースについて話す前に、ウェブサイトの展開方法について話しましょう。

### サーバーにWebサイトを展開します

まず、「Hugo -Minify`」を使用してWeb Staticファイル（生成されたディレクトリは公開）を生成し、「パブリック」ディレクトリのコンテンツをサーバーにコピーします（ファイル許可に注意してください）。次の `nginxを構成します`エージェント（ここで構成は「https」です。証明書がない場合は、` http`を構成することもできます））

```
server {
        listen 443;
        server_name aprilme.love;
        # 证书
        ssl_certificate "/yourPath/aprilme.love.pem";
        # 私钥
        ssl_certificate_key "/yourPath/aprilme.love.key";
        location / {
        	# 此处是你刚刚复制到的目录
                root /yourpath/blog;
                   }
        }
```

このようにして、ブラウザにドメイン名を入力してブログにアクセスできます。

また、次の構成（つまり、「http」のトラフィックをhttps」に転送するために、ポート80のフローをポート443に転送することもできます。「earridme.love」を独自のドメイン名に置き換えるように注意してください。

```
server {
        listen 80;
        server_name aprilme.love;
        rewrite ^(.*)$ https://${server_name}$1;
                }
```

証明書がない場合は、署名証明書を取得できます（ただし、ブラウザは、権威ある機関の署名ではなく、自分で署名されているため安全ではないことを示します）。証明書を購入することもできますが、現在のクラウドサーバープロバイダーは無料で無料で無料で送信して無料の証明書を送信します。たとえば、Alibaba Cloudのサーバーを参照できます。[2022 Alibaba Cloud Free SSL証明書アプリケーション（グラフィックの詳細な説明）-eriyun開発者コミュニティ（aliyun.com）](https://developer.aliyun.com/article/87550)エッセンス

### 構成「Github Action」

上記の展開プロセスは難しくありませんが、ブログコンテンツが更新されるときはいつでも、ファイルをコピーしてコピーする必要があります。これは非常に面倒です。ブログを書くときに自動的にリリースする方法はありますか。手動で公開する必要はありませんか？もちろん、「githubアクション」を使用しています。

#### 「githubアクション」

「GitHub Actions」は、GitHubプラットフォームが提供する自動ワークフローツールで、コードウェアハウスでさまざまな操作を自動的に実行します。開発者は、構成、テスト、展開、通知など、倉庫内の一連のイベントトリガーを構成し、定義することにより、ソフトウェア開発タスクを自動的に自動的に自動的に自動的に行うことができます。

「Github Actions」を使用すると、開発者はいくつかの簡単なYAMLファイルを作成してワークフローを定義できます。これらのワークフローは、特定のイベント（コードプッシュ、統合要求の作成、ラベルリリースなど）の場合に自動的にトリガーできます。ワークフローには、複数のステップ（ACTS）を含めることができます。各ステップは、コマンドの実行、コードの構築、テストの実行、他のコードウェアハウスへのプッシュ、通知の送信など、特定の操作を実行できます。

「GitHub Actions」は、Docker、AWS、Azure、Google Cloud、Slack、Jiraなど、他の多くの開発ツールやサービスと統合できる豊富な統合およびエコシステムを提供し、それによってより複雑な自動化ワークフローを実現します。

「Github Actions」は、開発者が開発効率を改善し、繰り返しタスクを自動化し、コードの品質を確保し、チームワークを促進するのに役立ちます。これは、GitHubプラットフォームの強力な機能であり、オープンソースプロジェクトや商業プロジェクトで広く使用されています。

#### 「githubアクション」

プロジェクトディレクトリに `.github/workflows`フォルダーを作成し、フォルダーの下に` my_blog_deploy.yaml`ファイルを作成します。ファイルのコンテンツは次のとおりです。

```yaml
name: Deploy Hugo Project to Aliyun ECS

on:
  push:
    branches:
      - main

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout code
      uses: actions/checkout@v2

    - name: Setup Hugo
      uses: peaceiris/actions-hugo@v2
      with:
        hugo-version: 'latest'

    - name: Build Hugo Site
      run: hugo --minify

    - name: Deploy Site to Aliyun ECS
      uses: easingthemes/ssh-deploy@v2
      env:
        SSH_PRIVATE_KEY: ${{ secrets.SSH_PRIVATE_KEY }}
        REMOTE_HOST: ${{ secrets.REMOTE_HOST }}
        REMOTE_USER: ${{ secrets.REMOTE_USER }}
        TARGET: /yourpath/blog
      with:
        source: public/
```

以下は、構成ファイルの説明です。

1.「名前」：「Hugo ProjectをAliyun ECSに展開する」という名前のワークフローの名前を指定します。
2. on`：「メイン」ブランチにプッシュするときにワークフローをトリガーするようにここで構成されているワークフローをトリガーするイベントを指定します。
3. Jobs`：「Deploy」と呼ばれるジョブを定義する1つ以上のジョブを定義します。
4.「runs-on」：作業操作のオペレーティングシステム環境を指定します。ここに「ubuntu-latest」があります。これは、最新のubuntu環境で実行されることを意味します。
5.ステップ：作業を定義するための一連のステップ。

 - 「名前」：各ステップの名前を指定して、ステップのステップを識別します。
-'USERS `：使用される指定されたアクション。ここでは、「アクション/チェックアウト@v2」アクションを使用してコードを検出するなど、複数の異なるアクションを使用して異なるタスクを実行し、「peaceiris/actions-chugo@v2」アクションインストールを使用してHugoを構成します、Alibaba Cloud ECSに「EasingThemes/ssh-deploy@v2」アクションのWebサイトを展開します。
-` with`：パラメーターを使用に渡すために使用されるアクションは、ここで異なるパラメーターを使用してHugoバージョンを構成し、ホスティングターゲット、ユーザー、およびパスを設定します。
-'Run`：現在の作業環境でコマンドを実行します。ここに「Hugo -Minify」コマンドがHugo Webサイトを構築し、出力を圧縮します。
-'ENV`：環境変数をセットアップします。SSH接続の秘密鍵とリモートホスト、ユーザー、およびターゲットパスを次に示します。これらの値はGitHub Secretから取得されます。

この構成ファイルの目的は、Hugo Webサイトを自動的に構築し、生成されたWebサイトファイルを、それぞれが「メイン」ブランチにプッシュするときにAlibaba Cloud ECSで指定された指定ディレクトリに展開することです。これにより、継続的な統合と自動展開を実現し、開発効率を改善し、Webサイトの最新バージョンがAlibaba Cloud ECSで利用できるようにすることができます。

上記の `$ {secrets.remote_host}`は、github倉庫の暗号化された環境変数であり、APIキー、プライベートキー、パスワードなどの機密情報を保存するために使用されます。以下はその設定方法です

1. GitHub倉庫を開き、倉庫ページの右上隅にある[設定]をクリックします。
2.倉庫の「設定」ページで、左メニューで「シークレット」を選択します。
3.「新しいリポジトリシークレット」ボタンをクリックして、新しい秘密を作成します。
4.秘密の名前と値を入力し、[秘密の追加]ボタンをクリックして保存します。
5. githubアクションのワークフロー構成ファイルでは、シークレットの構文を使用できます

前の構成ファイルでは、 `$ {secrets.ssh_private_key}`、 `$ {{secrets.remote_host}`、 `$ {{secrets.remote_user}}}を使用できます。情報は、展開およびその他の操作のために対応するGitHubアクションに安全に渡すことができます。

上記の構成の後、コードを倉庫にプッシュするたびに、「GitHub Action」が提供するサーバー内の構成ファイルのコンテンツを右および右に実行します。これにより、人工操作が大幅に簡素化され、複雑さが減少します。さらに、「githubアクション」は他の多くのことを行うことができ、機能は非常に強力です！

## 統合レビューシステム

ブログレビューシステムの重要性は、コンテンツと同じくらい重要です。また、好きなコメントシステムを選択することも重要です。いくつかの一般的なコメントシステムがあります

 - [アルタルク](https://artalk.js.org)
 - [カクタス](https://cactus.chat)
 - [cusdis](https://cusdis.com)
 - [disqu](https://disqus.com)
 - [Disqusjs](https://github.com/SukkaW/DisqusJ)
 - [ギスカス](https://giscus.app)
 - [gitalk](https://github.com/gitalk/gital)
 - [berem42](https://remark42.com)
 - [Twikoo](https://twikoo.js.org)
 - [発言者](https://utteranc.es)
 - [vssue](https://vssue.js.org)
 - [ワリン](https://waline.js.org)

私が現在選択しているのはcusdisです、理由は

1.オープンソースとセルフホスティング：Cusdisはオープンソースレビューシステムです。独自のサーバーでホストできます。完全なデータコントロールがあり、3番目のパーティサービスに依存しません。これは、ユーザーのプライバシーを保護し、コメントシステムを独立して管理および変更できることを意味します。
2.軽量：CusdisのSDKはわずか5kbです（GZIP圧縮後）。Disqusなどの他のコメントシステム（24kb GZIP圧縮後）と比較して、非常に軽量であり、ウェブサイトの負荷速度にあまりもたらされません。負担は、ウェブサイトのパフォーマンスを改善するのに役立ちます。
3.コメンテーターにログインを要求しないでください：Cusdisはコメンテーターにログインすることを要求しません。解説は、Cookieを使用せずに匿名のコメントをできます。これにより、ユーザーのログインと登録のしきい値を削減し、ユーザーの参加を増やすことができます。
4.使いやすい：Cusdisは、ウェブサイトの任意のページに簡単に埋め込むことができるシンプルな組み込みコメントツールを提供します。
5.電子メール通知：CUSDISはメール通知機能をサポートしており、Webサイト管理者が管理と回復のコメントを促進するために新しいコメント通知を時間内に受け取ることができます。

公式ウェブサイトとCusdisの展開に関する多くのブログは非常に明確に書かれています。私は主にCusdisのCross -Domainの問題についてここで話します。

### Cusdisの十字架の問題を解決します

ページがcusdisの埋め込みコードを参照すると、** cross -domain **の問題が発生しやすくなり、JSスクリプトまたはコメントデータをロードできません。

```html
<div id="cusdis_thread"
  data-host="https://yourhost"
  data-app-id="yourid"
  data-page-id="{{ PAGE_ID }}"
  data-page-url="{{ PAGE_URL }}"
  data-page-title="{{ PAGE_TITLE }}"
></div>
<script async defer src="https://yourhost/js/cusdis.es.js"></script>
```

この時点で、nginxに応答ヘッドを追加する必要があります

`add_header 'Access-Control-Allow-Origin' 'yourhost';`

これにより、ロードできない問題が解決しますが、コメントデータを読み込むときに問題があります。コメントデータの応答ヘッダーは、2つの「アクセス制御コントロールアロウオリジン「YourHost」で追加され、失敗につながります。データの読み込みの。

その理由は、HTTP要求が「オプション」を使用してコメントデータをロードする前にHTTPリクエストを作成するために使用されるためです。 。 nginxの構成を次の形式に書き込み、クロスドメインの問題を完全に解決します。セキュリティ上の考慮事項については、ウェブサイトがHTTPSを使用する場合、CusdisのホストもHTTPSを使用する必要があることに注意してください。

```
server {
        listen 443;
        ssl_certificate "your cert.pem";
        ssl_certificate_key "your cert.key";
        server_name yourhost;
        location / {
        proxy_pass http://127.0.0.1:3000;
        if ($uri !~* .*comments.*) {
        add_header 'Access-Control-Allow-Origin' '*';
        add_header 'Access-Control-Allow-Methods' 'GET, POST';
        add_header 'Access-Control-Allow-Headers' 'DNT,X-Mx-ReqToken,Keep-Alive,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,x-timezone-offset';}
        }}
```

## SEO、検索エンジン最適化

多くの記事では、Google、Bing、およびBaiduの検索エンジン最適化の操作ステップを最適化する方法を紹介しました。この部分については説明しません。検索エンジンの最適化に関する関連する知識について話させてください。

### 検索エンジンのインデックスは何ですか

検索エンジンのインデックスは、インターネット上の検索エンジンのレコードと、データベースに保存されているコンテンツを指します。インターネット上のインターネット上の検索エンジンをつかんで（またはクロール、クモ、クロールする）ことで独自のデータベースに保存されているため、検索時にユーザーが関連するWebページをすばやく見つけることができます。

検索エンジンのインデックスには通常、WebページのURL、タイトル、テキスト、リンク、写真、ビデオなどを含む大量のWeb情報が含まれています。この情報を介してエンジンのプロセスとインデックスを検索して、Webページ情報を保存および管理するための構造化されたデータベースを確立します。

ユーザーが検索のために検索エンジンにキーワードを入力すると、検索エンジンはインデックスデータベースのキーワードと一致し、Webページに関連する結果を返します。検索エンジンのインデックスの品質と精度は、検索結果の品質と精度に重要な影響を及ぼします。したがって、検索エンジン会社は、インデックスアルゴリズムとテクノロジーを継続的に改善し、より良い検索エクスペリエンスを提供します。

すべてのWebページが実際に検索エンジンによるものではないことに注意してください。検索エンジンは、キャプチャとインデックス戦略に基づいてWebページを選択的にインデックスを付け、Webページの品質、権限、更新頻度などの要因に応じてソートおよび表示することができます。 。エッセンスしたがって、ウェブサイト管理者は、一連の検索エンジン最適化（SEO）測定を通じてウェブサイトをインデックス化してランク付けする機会を改善できます。

### SEOとは何ですか

SEO（検索エンジン最適化）は検索エンジン最適化です。これは、Webサイトを最適化するコンテンツ、構造、技術を通じて検索エンジンのWebサイトのコンテンツを最適化する方法であり、それにより、WebサイトのWebサイトの可視性とトラフィックが増加します。検索結果ページ。 SEOの最適化は、より多くのターゲットトラフィックを取得するために、ウェブサイトが検索エンジンでより高いオーガニック（非PAID）検索ランキングを取得できるようにすることを目的としています。

SEOの最適化には通常、次の側面が含まれます。

1.キーワード調査：検索エンジンでユーザーが使用するキーワードを調べることにより、適切なキーワードを選択して、Webサイトのコンテンツに適用して、Webサイトがキーワードを使用してより高いランキングを取得するようにします。
2. Webサイトのコンテンツの最適化：タイトル、説明、テキストなどを含むWebサイトのコンテンツを最適化し、より品質、価値、関連性に関連し、検索エンジンの仕様と要件を満たします。
3. Webサイト構造の最適化：ウェブサイトの構造とレイアウトを最適化して、よりユーザーをよりユーザーにし、簡単にナビゲートして理解し、検索エンジンがWebサイトのコンテンツを効果的に把握できるようにします。
4.ウェブサイトのテクノロジーの最適化：ウェブサイトの読み込み速度、応答設計、URL構造、ページラベルなどを含むウェブサイトのテクノロジーを最適化して、ウェブサイトのユーザーエクスペリエンスを改善し、検索のクロール効果エンジン。
5.外部リンクの構築：外部リンクの構築を通じて、ウェブサイトのリンクの重みと人気を高めるため、検索エンジンでのウェブサイトの権限と信頼性が高まります。
6.ソーシャルメディアの最適化：ウェブサイトのコンテンツ、相互作用、参加など、ウェブサイトの露出と人気を高めるなど、ソーシャルメディアプラットフォームを通じて最適化されています。
7.監視と分析：WebサイトのSEO効果を定期的に監視および分析し、検索エンジンのWebサイトのランキングとトラフィックを理解し、データに基づいて調整および最適化します。

SEOの最適化の目標は、検索エンジンのWebサイトのランキングを改善して、ユーザーが関連するキーワードを検索するときに見つけやすくし、それによりWebサイトのオーガニックトラフィックを増やし、Webサイトのブランド認知度とビジネス転換率を高めることです。 。ただし、SEOは、継続的に最適化され、継続的な努力をする必要がある長期的かつ複雑な作業です。同時に、ウェブサイトが引き続き良いランキングを獲得できるようにするために、検索エンジンの仕様と要件に従う必要があります。検索エンジンで。

### sitemap.xmlとは何ですか

`sitemap.xml`は、Webサイトに使用されるXMLファイルであり、検索エンジンWebサイトのページとコンテンツに通知するためにWebサイトの構造化された情報が含まれています。これは、検索エンジンがウェブサイトをよりよく理解し、インデックスを作成するのに役立つ検索エンジン最適化（SEO）のテクノロジーです。

`sitemap.xml`ファイルには、通常、WebサイトのすべてのページのURLアドレス、およびこれらのページの重要性、頻度の更新、最終更新時間などの情報が含まれています。検索エンジンは、Webサイトのページをインテリジェントにキャプチャしてインデックスを作成するために、「sitemap.xml`ファイルを読み取ることにより、Webサイトの構造とコンテンツを理解できます。

`sitemap.xml`には、WebサイトのSEO最適化のための次の機能があります。

1.ウェブサイトのインデックス作成効果を改善する： `sitemap.xml`ファイルを検索エンジンに送信することにより、ウェブサイトのページをより適切にインデックスして表示するために、ウェブサイトのコンテンツをより包括的に検索するのに役立ちます。
2.新しいページのインデックス速度を加速：新しいページのURLを `sitemap.xml`ファイルに追加し、検索エンジンに送信して、ウェブサイトが新しいページをリリースした場合、速度を高速化できます検索エンジンによってインデックスが付けられている新しいページの。
3.検索エンジンをつかむ頻度を制御する： `sitemap.xml`ファイルでページの更新頻度と最終更新時間を設定することにより、検索エンジンプロンプトページの更新は、検索エンジンがよりインテリジェントに把握できるようにすることができますウェブサイトのページをよりインテリジェントにつかむ。
4.ウェブサイトのユーザーエクスペリエンスの向上： `sitemap.xml`ファイルを使用することにより、検索エンジンがウェブサイトの構造とコンテンツをよりよく理解するのを支援することができ、それによりユーザーが検索エンジンのウェブサイトページエクスペリエンスを見つけてアクセスすることができます。

## UMAMI自己加工フロー分析ツールを使用します

中国でゆっくりと使用されていた以前のGoogleアナリティクスは、データの損失を引き起こすのは簡単です。また、ユーザーデータを使用してGoogleユーザーのポートレートを生成します。だから私は選んだ[うーした](https://umami.is)代替として、ローカルエリアでの展開はより速く安全です。

### UMAMIはじめに

[うーした](https://umami.is) これは、シンプルで簡単なオープンソースWebサイトアクセストラフィック統計分析ツールです。 UMAMIはCookieを使用せず、ユーザーを追跡せず、収集されたすべてのデータはGDPRポリシーに沿った匿名で処理されます。リソースは非常に低いです。機能は単純ですが、分析データは非常にリッチです。システム、機器、Webページが訪問されました。また、Google Analytics、CloudFlare Web Analytics、CNZZ、51LA、その他の統計ツールを置き換えるために使用できる多言語もサポートしています。また、統計データをより正確にするためにブロックによって回避することもできます（**後で発見しました。部分的に広告を出してください。プラグインインターセプト... **）。[[UMAMI自己加工Webサイトトラフィック統計分析ツールからの引用-ATPX](https://atpx.com/blog/build-umami-web-analytics)]

### umamiを展開する方法

なぜなら[UMAMI公式文書](https://umami.is/doc)壊れているので、それに移動してください[オープンソースウェアハウス](https://github.com/umami-software/umam)展開ドキュメントを確認すると、操作はまだ非常に高速です。ここでは、遭遇しやすい問題について説明します。

まず第一に、クローン化されたgithub倉庫「git clone https：// github.com/umami-software/umami.git`が発生しやすいとき。この時点で、最初に倉庫をダウンロードして、指定されたディレクトリに減圧することができますサーバーの場合、Github倉庫をGiteeにコピーしてから、Gitee Warehouseをクローンすることもできます。しかし、Giteeには1つだけです[同期倉庫](https://gitee.com/873098424/umami/tree/maste)したがって、Gitee Warehouseへのリンクを直接変更できます[住所](https://gitee.com/873098424/umami/tree/maste)、多くのトラブルを救います。現時点でのコマンドはです

```bash
git clone https://gitee.com/873098424/umami.git
```

その後、チュートリアルに従ってください。 「Yarn build」が必要になる前に、データベースにumamiが存在しない場合はデータベースを作成します。umamiデータベースを作成し、構成ファイルのライブラリの名前をUmamiに変更します（作成したデータベース名と同じです）本質次に**テーブルを作成するために提供されたSQLステートメントを使用しないでください。

その後、ビルドを実行してスタートを実行します（開始がポート職業によるものの場合、 `Yarn Start -Port = 3001`を使用してポートを変更できます）。このサービスは開始しても開始されます。 nginxを構成する方法、ログイン、パスワードの変更などについては、このブログを参照できます[Umami自己構築のウェブサイトトラフィック統計分析ツールを使用する-ATPX](https://atpx.com/blog/build-umami-web-analytics)エッセンス

この時点で、Umamiはそれを正常に使用できるはずです。コンソールが間違ったリソースをロードできなかった場合、net :: err_blockd_by_client`をプロンプトする場合、Adblockなどの広告インターセプターによってブロックする必要があります。それを解決するようになりますが、広告インターセプターのインターセプターを回避する良い方法はないので、データがそれほど正確ではないかもしれません。

## 要約します

上記のコンテンツを読んだ後、私はあなたがあなた自身のブログを作成する基本的なプロセスに精通していると信じています。**理解は非常に重要であり、練習も同様に重要です。環境、選択のテーマ、個人的な経験のために、個人的なブログを構築する過程で、遭遇する問題は異なる必要があります。このプロセスで最も重要なことは、**忍耐**であり、遭遇した問題を解決し、学習で成長し、成長を学ぶために時間を費やすことをいとわない。この記事の表紙と同じように、モネのウォーターリリーは静けさと忍耐を象徴しています。また、自分のブログを作成したいすべての学生と目標を達成したい学生を願っていますが、問題を発見して解決し、問題を解決するのに十分な忍耐と能力がある限り、すべてがスムーズになることは不可能です。問題を解決し、問題を解決します。外の世界を助けることができない場合は、外の世界から助けを求めてください。**は間違いなく何かを手に入れ、達成されます。 **