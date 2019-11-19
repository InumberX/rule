# Styloose - CSS Loose Naming Convention

## 概要

本ドキュメントはCSSのクラス命名規則を定義したものです。
命名規則とありますが、作業を行う上でこの規則を必ずしも守る必要はありません。
基本的には本規則に沿って命名を行いますが、例外としてこの規則外の命名を行っても問題ありません。
緩く、臨機応変に使用できる命名規則を目指し、本命名規則を定義します。

## 基本ルール

* BEMをベースとしたクラス命名を行います。
* 単語は「-（ハイフン）」で連結します。
* BlockとElementは「_（アンダーバー）」で連結します。
* Modifierは「__（アンダーバー2つ）」を先頭に付け、BlockまたはElementと複合クラスで使用します。

### サンプル

#### HTML

```
<ul class="list-sample">
<li class="list-sample_item">〜</li>
<li class="list-sample_item">〜</li>
<li class="list-sample_item __wide">〜</li>
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

.list-sample_item.__wide {
width: 100%;
}
```
