# positionプロパティまとめ

https://zero-plus.io/media/positioning-elements-by-position/

要素の「位置」を指定する際に使用するCSSプロパティです。

- 要素を自由に配置したい
- 要素の重なり順を変えたい
- ヘッダーを固定して表示したい

基本的に`top`,`bottom`,`left`,`right`のプロパティで位置を指定して使う

`top:0;`と`left:0;`だとその要素は基準の左上に配置される

※多分大体は`top`と`left`だけでOK

## static

staticは初期値です。要素に対しpositionプロパティを何も指定されていない場合はstatic。

staticを使用するのは、レスポンシブ対応などでpositionプロパティを解除する場面です。

## relatieとabsolute

親要素にrelativeを指定して基準にし、子要素にabsoluteを指定することで、子要素を移動します。  

## fixed

Webサイトをスクロールしても、fixedを適用した要素はスクロールに追従し、常に画面上の決まった位置に固定されます。

指定方法・特徴はabsouteとほぼ同じと考えてOKです。`基準がページ全体になる`ことに注意しましょう。画面左上からどれだけの距離に配置するか考えるとイメージがしやすいかと思います。

## sticky

スクロールした際に要素を粘着させ、固定表示することができます。

親要素内で固定

要素の高さは有する

position: sticky; を適用した要素は、スティッキーアイテムといいます。position: sticky; が適用された要素の「親要素」は、スティッキーコンテナといいます。

![image](https://github.com/naoyuki2/TIL/assets/135786069/6d06fbdd-34f0-4df4-897b-1837200c9e5e)

