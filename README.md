Advanced RecyclerView
===============

> **Fork notice:** This is a fork of [h6ah4i/android-advancedrecyclerview](https://github.com/h6ah4i/android-advancedrecyclerview).
> It is **not distributed via Maven**. The library must be built manually.
> Its primary purpose is to serve as the native Android dependency for the
> [Xamarin.Bindings.AdvancedRecyclerView](https://github.com/thefex/Xamarin.Bindings.AdvancedRecyclerView) (.NET Android) project.

This RecyclerView extension library provides Google's Inbox app like swiping, Play Music app like drag-and-drop sorting and expandable item features.

---

Changelog
---

### 1.4.0 *(current)*
- Migrated to AndroidX (`androidx.recyclerview:recyclerview:1.4.0`)
- Upgraded Gradle wrapper to 8.9 and Android Gradle Plugin to 8.6.1
- Replaced deprecated `jcenter()` with `google()` + `mavenCentral()`
- Replaced deprecated `maven` + `uploadArchives` with `maven-publish` plugin
- Updated `compileSdk` to 35, `minSdk` to 14 (library) / 21 (example app)
- Java source/target compatibility updated to 1.8
- Dropped unused dependencies (`com.android.support:design`, `vector-compat`)

---

Versioning
---

The version of this library is aligned with the **androidx RecyclerView version** it depends on.
Current version: **1.4.0** (tracks `androidx.recyclerview:recyclerview:1.4.0`)

---

Building
---

This library is not published to any Maven repository. To use it, build the AAR manually:

```bash
./gradlew :library:assembleRelease
```

The output AAR will be located at:

```
library/build/outputs/aar/library-release.aar
```

Add the AAR to your project as a local dependency.

---

Target platforms
---

- API level 14 or later

---

Usage
---

Please check the implementation of the simple examples.

- [Drag & Drop example](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_d/)
- [Swipe example](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_s/)
- [Expandable item example](example/src/main/java/com/h6ah4i/android/example/advrecyclerview/demo_e/)


Primary classes/interfaces
---

### Drag & Drop related classes/interfaces

| Class/Interface name                  | Description                                              |
|---------------------------------------|----------------------------------------------------------|
| [`RecyclerViewDragDropManager`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/draggable/RecyclerViewDragDropManager.java)         | Provides Drag & Drop sort operation                      |
| [`DraggableItemAdapter<T>`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/draggable/DraggableItemAdapter.java)             | Implement this interface on your RecyclerView.Adapter    |
| [`DraggableItemViewHolder`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/draggable/DraggableItemViewHolder.java)             | Implement this interface on your RecyclerView.ViewHolder |


### Swiping related classes/interfaces

| Class/Interface name                  | Description                                              |
|---------------------------------------|----------------------------------------------------------|
| [`RecyclerViewSwipeManager`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/swipeable/RecyclerViewSwipeManager.java)            | Provides Swipe operation                             　  |
| [`SwipeableItemAdapter<T>`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/swipeable/SwipeableItemAdapter.java)             | Implement this interface on your RecyclerView.Adapter    |
| [`SwipeableItemViewHolder`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/swipeable/SwipeableItemViewHolder.java)             | Implement this interface on your RecyclerView.ViewHolder |


### Expandable item related classes/interfaces

| Class/Interface name                  | Description                                              |
|---------------------------------------|----------------------------------------------------------|
| [`RecyclerViewExpandableItemManager`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/expandable/RecyclerViewExpandableItemManager.java)   | Provides Expandable item function                    　  |
| [`ExpandableItemViewHolder`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/expandable/ExpandableItemViewHolder.java)            | Implement this interface on your RecyclerView.ViewHolder |
| [`ExpandableItemAdapter<GVH, CVH>`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/expandable/ExpandableItemAdapter.java)     | Implement this interface on your RecyclerView.Adapter    |
| [`ExpandableDraggableItemAdapter<GVH, CVH>`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/expandable/ExpandableDraggableItemAdapter.java) | (optional) Implement this interface on your RecyclerView.Adapter to support Drag & Drop sort operation |
| [`ExpandableSwipeableItemAdapter<GVH, CVH>`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/expandable/ExpandableSwipeableItemAdapter.java) | (optional) Implement this interface on your RecyclerView.Adapter to support Swipe operation |



### RecyclerView decorations

| Class/Interface name                  | Description                                              |
|---------------------------------------|----------------------------------------------------------|
| [`ItemShadowDecorator`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/decoration/ItemShadowDecorator.java)                 | Drop shadow decoration for pre-Lollipop devices          |
| [`SimpleListDividerDecorator`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/decoration/SimpleListDividerDecorator.java)          | Simple list divider decoration                           |


### Misc.

| Class name                                 | Description                                              |
|--------------------------------------------|----------------------------------------------------------|
| [`RecyclerViewTouchActionGuardManager`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/touchguard/RecyclerViewTouchActionGuardManager.java)      | Suppress scrolling while item animations are running     |
| [`AbstractDraggableItemViewHolder`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/utils/AbstractDraggableItemViewHolder.java)          | ViewHolder class which implements boilerplate code of the  `DraggableItemViewHolder` interface      |
| [`AbstractSwipeableItemViewHolder`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/utils/AbstractSwipeableItemViewHolder.java)          | ViewHolder class which implements boilerplate code of the  `SwipeableItemViewHolder` interface      |
| [`AbstractExpandableItemViewHolder`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/utils/AbstractExpandableItemViewHolder.java)            | ViewHolder class which implements boilerplate code of the  `ExpandableItemViewHolder` interface      |
| [`AbstractDraggableSwipeableItemViewHolder`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/utils/AbstractDraggableSwipeableItemViewHolder.java) | ViewHolder class which implements boilerplate code of the `DraggableItemViewHolder` and the `SwipeableItemViewHolder` interfaces      |
| [`AbstractExpandableItemAdapter<GVH, CVH>`](library/src/main/java/com/h6ah4i/android/widget/advrecyclerview/utils/AbstractExpandableItemAdapter.java)  | Adapter class which implements boilerplate code of the `ExpandableItemAdapter` interface |


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
