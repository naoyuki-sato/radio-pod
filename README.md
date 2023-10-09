# radio-pod

* crontabにコマンドを追加
  * 例) 40 8 * * 7 /home/naoyuki/work/update_podcast_data/update_podcast_data.sh light
    * 「分」「時」「日」「月」「曜日」
    * 0=日、1=月、2=火、3=水、4=木、5=金、6=土、7=日
* update_podcast_data.shのために
  * get_radiko_data.pyを編集
    * スクリプトを呼び出して、Radikoのコンテンツを保存する
    * 先頭のJSONに追加したい番組を追加する
    * 曜日は5が土曜
    * コンテンツを保存するディレクトリーは手動で作成
  * update_podcasrt_xml.py
    * 上記でダウンロードされたコンテンツから、podcast用のXMLを作成する
    * 先頭のJSONに情報を追加
    * 画像イメージなどは自分で準備
