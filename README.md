# imagescaling
画像拡縮アルゴリズムの見た目比較ツール

### 対応アルゴリズム
- Nearest neighbor
- Bilinear
- Bicubic
- LanczosN
- Spline16,36

### スクリーンショット

![Screenshot](https://github.com/suconbu/imagescaling/blob/master/screenshot1.png)

### 操作方法

| 操作 | 説明 |
| -- | -- |
| 矢印キー左右 | 画像を切り替える |
| 画像をクリック | ポップアップをキープする |
| アルゴリズム名(bilinearなど)をダブルクリック | そのアルゴリズムを非表示にする |

### メモ
画像や倍率はこのあたりで変更できます。

```javascript
  // imagescaling.html
  const resizeFunctionMap = {
    //nearest: {func: resizeByNearest, parameter: null},
    bilinear: {func: resizeByBilinear, parameter: null},
    bicubic: {func: resizeByBiqubic, parameter: null},
    // lanczos2: {func: resizeByLanczos, parameter: 2},
    lanczos3: {func: resizeByLanczos, parameter: 3},
    spline16: {func: resizeBySpline, parameter: 2},
    spline36: {func: resizeBySpline, parameter: 3},
  }
  const resizeRatios = [1.0, 1.3, 1.7, 2.0, 2.3, 2.7, 3.0];
```
