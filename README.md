# Grid-Horizontal
Automatically adjust the number of rows with height.
# The first part
![IMG_1172](https://github.com/S-way520/Grid-Horizontal/assets/95877651/35bb5766-d6e1-4902-8994-cb7e5d6b8133)
# The second part
Code file 1
```swift
import SwiftUI
@main
struct MyApp: App {
    var body: some Scene {
        WindowGroup {
            ContentView()
        }
    }
}
```
Code file 2
```swift
import SwiftUI
struct ContentView: View {
    @State private var gridColumns: [GridItem] = [GridItem(.adaptive(minimum: 200), spacing: 0)]
    var body: some View {
        ScrollView(.horizontal) {
            LazyHGrid(rows: gridColumns, spacing: 10) {
                Rectangle()
                    .frame(width: 400, height: 200)
                    .foregroundColor(.red)
                Rectangle()
                    .frame(width: 400, height: 200)
                    .foregroundColor(.green)
                Rectangle()
                    .frame(width: 400, height: 200)
                    .foregroundColor(.gray)
                Rectangle()
                    .frame(width: 400, height: 200)
                    .foregroundColor(.orange)
                Rectangle()
                    .frame(width: 400, height: 200)
                    .foregroundColor(.blue)
                Rectangle()
                    .frame(width: 400, height: 200)
                    .foregroundColor(.cyan)
            }
            .padding()
        }
        .frame(height: 450)
    }
}
```
