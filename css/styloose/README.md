# Styloose - CSS Loose Naming Convention

## 概要

本ドキュメントはCSSのクラス命名規則を定義したものです。
命名規則とありますが、作業を行う上でこの規則を必ずしも守る必要はありません。
基本的には本規則に沿って命名を行いますが、例外としてこの規則外の命名を行っても問題ありません。
緩く、柔軟に使用できるものを目指し、本命名規則を定義します。

## 基本ルール

* BEMをベースとしたクラス命名を行います。
* 単語は「-（ハイフン）」で連結します。<br>例）sample-name
* BlockとElementは「_（アンダーバー1つ）」で連結します。
  例）block-name_element-name
* Modifierは「is-」を先頭に付け、BlockまたはElementと複合クラスで使用します。
  例）is-modifier-name
* CSSのセレクタは単一または複合を基本とします。
* JavaScriptで処理を行うクラスは「js-」を接頭語として付けます。
  例）js-trigger-btn
* 単語はなるべく省略して命名することを推奨します。
  例）header → hs, button → btn, contents → cnt, image → img, title → ttl, text → tx

### サンプル

#### HTML

```
<ul class="list-sample">
<li class="list-sample_item">〜</li>
<li class="list-sample_item">〜</li>
<li class="list-sample_item is-wide">〜</li>
</ul>
```

#### CSS

```
.list-sample {
 list-style: none;
 margin: 0;
 padding: 0;
 display: flex;
 flex-wrap: wrap;
}

.list-sample_item {
 width: 50%;
}

.list-sample_item.is-wide {
 width: 100%;
}
```
