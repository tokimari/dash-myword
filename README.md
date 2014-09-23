# Dash用Docsetで英単語録

英語がからきし駄目なので、勉強用に英単語録を日報で配信し続けています。

自分が後から探しやすいように、
その[英単語録](https://github.com/tokimari/myword "英単語録")を呼び出すための、Dash用ドックセットを作りました。

Dash内で<code>mw:</code>で検索できます。

index追加の仕方：
```
$ cd myword.docset/Contents/Resources/
$ sqlite3 docSet.dsidx
sqlite> INSERT OR IGNORE INTO searchIndex(name, type, path) VALUES (word, entry-type, path-to-word);
```

* entry-type: [entry-type](http://kapeli.com/docsets#supportedentrytypes "Supported Entry Types")
* path-to-word: Documents/からの相対パス or 絶対パス（URL）
