# Styloose - CSS Loose Naming Convention

## 概要

本ドキュメントはCSSのクラス命名規則を定義したものです。
命名規則とありますが、作業を行う上でこの規則を必ずしも守る必要はありません。
基本的には本規則に沿って命名を行いますが、例外としてこの規則外の命名を行っても問題ありません。
緩く、柔軟に使用できるものを目指し、本命名規則を定義します。

## 基本ルール

* BEMをベースとしたクラス命名を行います。
* 単語は「-（ハイフン）」で連結します。
  例）sample-name
* BlockとElementは「__（アンダーバー2つ）」で連結します。
  例）block-name__element-name
* Modifierは「-（ハイフン）」を先頭に付け、BlockまたはElementと複合クラスで使用します。
  例）-modifier-name
* CSSのセレクタは単一または複合を基本とします。
* 状態を表すクラスは「is-」を接頭語として付けます
  例）is-active
* JavaScriptで処理を行うクラスは「js-」を接頭語として付けます
  例）js-trigger-btn

### サンプル

#### HTML

```
<ul class="list-sample">
<li class="list-sample__item">〜</li>
<li class="list-sample__item">〜</li>
<li class="list-sample__item -wide">〜</li>
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

.list-sample__item {
 width: 50%;
}

.list-sample_item.-wide {
 width: 100%;
}
```
