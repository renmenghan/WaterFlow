# WaterFlow
瀑布流
## 拖入WaterFlowLayout.h.m即可使用
* 创建布局为WaterFlowLayout
```
 WaterFlowLayout *layout = [[WaterFlowLayout alloc] init];
 UICollectionView *collectionView = [[UICollectionView alloc] initWithFrame:self.view.bounds collectionViewLayout:layout];
```
## 本框架还提供了以下代理方法供实现
### 必须实现的代理方法
```
- (CGFloat)WaterFlowLayout:(WaterFlowLayout *)WaterFlowLayout heightForRowAtIndex:(NSUInteger)index itemWidth:(CGFloat)itemWidth;
// 此代理方法返回为item的高度 必须实现
```

```
@optional
- (CGFloat)columnCountInWaterflowLayout:(XMGWaterflowLayout *)waterflowLayout;
- (CGFloat)columnMarginInWaterflowLayout:(XMGWaterflowLayout *)waterflowLayout;
- (CGFloat)rowMarginInWaterflowLayout:(XMGWaterflowLayout *)waterflowLayout;
- (UIEdgeInsets)edgeInsetsInWaterflowLayout:(XMGWaterflowLayout *)waterflowLayout;

// 以上代理方法分别 实现 列数 行列间距 内边距
```
