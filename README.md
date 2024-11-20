---

# **SFSymbols**

A Swift Package providing a type-safe and iterable `enum` for **SF Symbols**, simplifying their use in SwiftUI and UIKit projects. It includes an extension for `Image` (SwiftUI) to easily create images using SF Symbols.

---

## **Features**

- **Type-safe SF Symbols Access:** Use the `SFSymbol` enum to reference symbols by name without relying on string literals.
- **Iterable Enum:** Supports iteration through all available SF Symbols using `CaseIterable`.
- **SwiftUI Integration:** Effortlessly create `Image` views with SF Symbols via a custom initializer.

---

## **Installation**

### **Swift Package Manager SPM**

1. In Xcode, go to `File > Add Packages...`.
2. Enter the repository URL:

   ```
   https://github.com/AP-94/SFSymbols
   ```

3. Add the package to your project.

---

## **Usage**

### **Using the `SFSymbol` Enum**

The `SFSymbol` enum provides a list of pre-defined SF Symbols for type-safe access.

```swift
import SFSymbols

// Access an SF Symbol
let symbolName = SFSymbol.heart.rawValue // "heart"

// Iterate through all symbols
for symbol in SFSymbol.allCases {
    print(symbol.rawValue)
}
```

---

### **Creating a SwiftUI `Image` with an SF Symbol**

The `Image` extension makes it simple to create views with SF Symbols:

```swift
import SFSymbols
import SwiftUI

struct ContentView: View {
    var body: some View {
        VStack {
            Image(symbol: .heart)
                .font(.system(size: 50))
                .foregroundColor(.red)

            Image(symbol: .gear)
                .font(.system(size: 50))
                .foregroundColor(.gray)
        }
    }
}
```

---

## **Requirements**

- **iOS 13.0+** / **macOS 11.0+**
- **Xcode 12.0+**
- **Swift 5.7+**

---

## **Contributing**

Contributions are welcome! If you have additional SF Symbols to include or ideas for improvements, feel free to open an issue or submit a pull request.

---

## **License**

This project is licensed under the MIT License. See file [here](https://github.com/AP-94/SFSymbols/blob/main/LICENSE).

---
