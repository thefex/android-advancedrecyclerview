Advanced RecyclerView
===============

> **Fork Notice**
>
> This is a maintained fork of [h6ah4i/android-advancedrecyclerview](https://github.com/h6ah4i/android-advancedrecyclerview).
> **This fork is not published to Maven** and is solely intended to be consumed as an Android library
> in [.NET Android (Xamarin.Android) bindings](https://learn.microsoft.com/en-us/previous-versions/xamarin/android/platform/binding-java-library/) projects.
> If you need a Maven-published artifact, refer to the original repository.

---

This RecyclerView extension library provides Google's Inbox app like swiping, Play Music app like drag-and-drop sorting and expandable item features. Works on API level 21 or later.

---

### Demonstration video on YouTube

<a href="http://www.youtube.com/watch?feature=player_embedded&v=S7cSwMArjUQ" target="_blank">
<img src="http://img.youtube.com/vi/S7cSwMArjUQ/0.jpg" alt="Advanced" width="480" height="360" border="10" />
</a>

---

Target platforms
---

- API level 21 or later


Latest version
---

- Version 1.4.0  ([RELEASE NOTES](./RELEASE-NOTES.md))


Versioning
---

Library versions are aligned with the **androidx.recyclerview** version they are built against.
For example, version `1.4.0` of this library is built with `androidx.recyclerview:recyclerview:1.4.0`.

| Library version | androidx.recyclerview version |
|-----------------|-------------------------------|
| 1.4.0           | 1.4.0                         |

See [RELEASE-NOTES.md](./RELEASE-NOTES.md) for the full changelog.


Getting started
---

This library is consumed directly from source as part of a .NET Android (Xamarin.Android) bindings project.
Clone or add this repository as a Git submodule and reference the `:library` module from your project.

```gradle
// settings.gradle
include ':advancedrecyclerview'
project(':advancedrecyclerview').projectDir = new File('../android-advancedrecyclerview/library')

// app/build.gradle
dependencies {
    implementation project(':advancedrecyclerview')
}
```

---

Examples
---

Please check the implementation of the simple examples.

### Drag & Drop related examples

- [Basic](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_d_basic/)
- [Minimal](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_d_minimal/)
- [Draggable grid](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_d_grid/)
- [Draggable staggered grid](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_d_staggered_grid/)
- [Draggable with section](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_d_with_section/)
- [Drag on Long press](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_d_on_longpress/)
- [Uses onCheckCanDrop()](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_d_check_can_drop/)

### Expandable item related examples

- [Basic](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_e_basic/)
- [Minimal](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_e_minimal/)
- [Add & Remove item](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_e_add_remove/)
- [Already expanded groups](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_e_already_expanded/)

### Swipeable related examples

- [Basic](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_s_basic/)
- [Minimal](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_s_minimal/)
- [Swipeable with button](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_s_button/)
- [Vertical](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_s_vertical/)
- [Viewpager](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_s_viewpager/)
- [Swipe on long press](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_s_longpress/)

### Headers and Footers examples
- [Minimal](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_hf_minimal)
- [Expandable with Header/Footer](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_hf_e)
- [Add & Remove Header/Footer items](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_hf_add_remove)

### WrapperAdapter examples
- [Composition of All Features](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_composition_all)
- [Insertion items](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_wa_insertion)
- [Filtering items](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_wa_filtering)

### Hybrid examples

- [Draggable & Swiping](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_ds/)
- [Draggable & Swiping with section](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_ed_with_section/)
- [Expandable & Draggable & Swiping](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_eds/)

### Other examples

#### iOS Mail app like swipe action

<img src="images/other_example_ios_mail.png" width="200" />

- [Repository](https://github.com/h6ah4i/RecyclerViewiOSMailAppLikeSwipe)

---

License
---

This library is licensed under the [Apache Software License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).

See [`LICENSE`](LICENSE) for full of the license text.

    Copyright (C) 2015 Haruki Hasegawa

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
