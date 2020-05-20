# Styloose - CSS Loose Naming Convention

## 概要

本ドキュメントは CSS のクラス命名規則を定義したものです。
命名規則とありますが、作業を行う上でこの規則を必ずしも守る必要はありません。
基本的には本規則に沿って命名を行いますが、例外としてこの規則外の命名を行っても問題ありません。
緩く、柔軟に使用できるものを目指し、本命名規則を定義します。

## 基本ルール

- BEM をベースとしたクラス命名を行います。
- 単語は「-（ハイフン）」で連結します。<br>例）sample-name
- Block と Element は「\_（アンダーバー 1 つ）」で連結します。<br>例）block-name_element-name
- Modifier は「is-」を先頭に付け、Block または Element と複合クラスで使用します。<br>例）is-modifier-name
- CSS のセレクタは単一または複合を基本とします。
- JavaScript で処理を行う要素は「data-js」属性を付与します。<br>例）data-js="accordion-btn", data-js="accordion-cnt"
- 単語はなるべく省略して命名することを推奨します。<br>例）header → hd, button → btn, contents → cnt, image → img, title → ttl, text → tx

### サンプル

#### HTML

```
<ul class="list-sample">
<li class="list-sample_item">〜</li>
<li class="list-sample_item">〜</li>
<li class="list-sample_item is-wide">〜</li>
</ul>
```

#### Sass（SCSS）

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

 &.is-wide {
  width: 100%;
 }
}
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
 margin: 0;
 padding: 0;
}

.list-sample_item.is-wide {
 width: 100%;
}
```
