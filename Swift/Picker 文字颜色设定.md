设定 DatePicker 时（Wheel 模式），即便用 `.tint()` 指定一种颜色，其也将收到系统深浅色模式影响。但是，[这么做](https://swiftuirecipes.com/blog/styling-swiftui-datepicker)却可以：

```Swift
extension View {
    @ViewBuilder
    func applyDatePickerTextColor(_ color: Color) -> some View {
        if UITraitCollection.current.userInterfaceStyle == .light {
            self.colorInvert().colorMultiply(color)
        } else {
            self.colorMultiply(color)
        }
    }
}
```