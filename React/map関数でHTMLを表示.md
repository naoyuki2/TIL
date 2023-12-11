```
  return (
      <>
          {items.map((item: ItemType) => {
              return (
                  <div key={item.date}>
                    <h1>{item.date}</h1>
                  </div>
              )
          })}
      </>
  )
```
itemsは一つ以上のJSON形式だとする。itemsをmapにかけて、itemとして、一つずつ受け取る。その際に一意のkeyを設定する必要がある。なんかReactの差分レンダリングっていう機能によって変わった所だけ更新するっていうのがあるの。それが一意のkeyがないとどこが変わったかどうか分からんらしい。
