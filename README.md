# Synodic Style Guide

SwiftUI Style Guide for Synodic Studio

## Naming Views

Prefer ending view names with `View` except for some special cases. If the view is normally used in a `List` or `Form` then the view should end with `Row`. If the view is intended to be an entire page then the name should end in `Page`. If the top-level view of a custom view builds on (or behaves like) a built-in view then it can be named that way, such as `ItemsList`, but not `ItemsSection` because a `Section` must be within a List to behave properly. If necessary, use a static `header` or `footer`, for example, to be used in the parent view that does have a `List` and `Section`. Groups should be named regular title case and spacing.

### `Section` Idea

What about an extension or similiar like `.asSection` that can put the child view inside of a section? Something like:

```swift
MyView()
	.inListSection() // or `.forSection` or `.asSection` etc.
```

equivalent to

```swift
Section() {
	MyView()
} header: {
	MyView.header
} footer: {
	MyView.footer
}
```

## References

* [Ray Wenderlich Swift Style Guide](https://github.com/raywenderlich/swift-style-guide)
* [Google Swift Style Guide](https://google.github.io/swift/)
* [Ultimate Swfit Code Style Guidelines](https://github.com/lazarevzubov/Ultimate-Swift-Code-Style-Guidelines) [(about)](https://betterprogramming.pub/finding-the-ultimate-swift-code-style-guidelines-59025a7c163c)
* [Swift API Guidelines](https://www.swift.org/documentation/api-design-guidelines/)