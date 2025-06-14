nil 表示缺失。Swift 的 nil 和 Objective-C 中的 nil 不一样：
- 在 Objective-C 中，nil 是一个指向不存在对象的指针。
- 在 Swift 中，nil 不是指针——它是一个确定的值，用来表示值缺失。
- 任何类型的可选状态都可以被设置为 nil，不只是对象类型。