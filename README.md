<script src="https://cdn.jsdelivr.net/npm/tify@0.27.0/dist/tify.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/list.js/2.3.1/list.min.js"></script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/tify@0.27.0/dist/tify.css">

# ta-niiyan.github.io

It's readme file.
Code4Lib JAPAN2022カンファレンスでつくってみました

## おしらせ

- サイトをオープンしました（2022.9.3）
- 新着図書がはいりました（2022.9.3）

## 新着図書一覧

<div id="books">
  <input class="search" placeholder="検索" />
  <button class="sort" data-sort="title">
    タイトルで並べ替え
  </button>
  <ul class="list">
    <!-- _data フォルダの books.csv からデータを取り出す -->
    {% for book in site.data.books %}
      <li>
        <!-- books.csv の title 列、 url 列をリンク先に設定 -->
        <p class="title"><a href="{{ book.url }}">{{ book.title }}</a></p>
      </li>
    {% endfor %}
  </ul>
</div>

## リンク
- [Code4Lib JAPAN Conference 2022](https://wiki.code4lib.jp/wiki/C4ljp2022)

<script>
var options = {
    valueNames: [ 'title' ]
};

var userList = new List('books', options);
</script>
