# ReusableView
![Swift](https://img.shields.io/badge/Swift-4.0-orange.svg)

ReusableView提供了通用的register cell的方法，避免写死字符串

## Example
* 注册重用的cell

```swift
collectionView.register(SomeCollectionViewCell.self)
collectionView.register(SomeSectionView.self,
                        forSupplementaryViewOfKind: UICollectionElementKindSectionHeader)
collectionView.register(SomeView.self,
                        forSupplementaryViewOfKind: UICollectionElementKindSectionHeader)

self.register(SomeSeparatorView.self,
              forDecorationViewOfKind: SomeSeparatorView.defaultReuseIdentifier)                        
```
* 获取重用cell

```swift
let cell: SomeCollectionViewCell = collectionView.dequeueReusableCell(for: indexPath)
let view: SomeSectionView = collectionView.dequeueReusableSupplementaryView(ofKind: kind, for: indexPath)
```