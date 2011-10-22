* ディレクトリの構成

. <PROJECT_HOME>
	プロジェクトホームディレクトリ
pages/
    DokuWikiフォーマットで書かれたテキスト。
media/
	pages内のテキストで使用されるグラフィックス類。

* ローカルなDokuWikiへの配備方法

pagesディレクトリーのシンボリックリンク
DokuWiki上での名前空間を(PROJECT_X)とします。

# cd <DOKUWIKI_DATA_DIR>/pages
# ln -s <PROJECT_HOME>/pages ./PROJECT_X

# cd <DOKUWIKI_DATA_DIR>/media/PROJECT_X
# ln -s <PROJECT_HOME>/media ./PROJECT_X

browse
http://localhost/dokuwiki/doku.php?id=PROJECT_X:

* 公開サイトへの転送例
転送先サーバー: <SERVER>
転送先DokuWikiデータディレクトリ: <DOKUWIKI_DATA_DIR>

# cd <PROJECT_HOME>
# scp -rp -P 222 pages apache@<SERVER>:<DOKUWIKI_DATA_DIR>/pages/PROJECT_X
# scp -rp -P 222 media apache@<SERVER>:<DOKUWIKI_DATA_DIR>/media/PROJECT_X

browse
http://test02.knowd.co.jp/dokuwiki/doku.php?id=PROJECT_X:

