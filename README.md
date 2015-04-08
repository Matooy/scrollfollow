要素をスクロールに追随させます。

### How to use.

```javascript
$(el).scrollfollow({
  wrapper      : $(document),  // Scroll を監視したい要素。指定しない場合は $(document) の scroll イベントを監視。
  anim_length  : 200,          // (px) toggle_anim が呼ばれるstart_marginからの距離。
  bottom       : 0,            // (px) 下に着いて止まるまでの間、画面上の bottom 値を維持します。
  start_margin : 0,            // (px) 開始位置はここで調整。
  stop_margin  : 200,          // (px) どこまでついて行くかはここで調整。（ex.最下部から200pxで追随を終了。
  toggle_anim  : function(frame, el){
                   // frame : 0~start_margin の値がスクロールに応じて渡ってきます。
                   // el    : 要素
                   el.css({
                     opacity: (frame - 20) / 360
                   });
                 }
});
```
