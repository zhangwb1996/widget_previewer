# widget_perviewer

[English](./README.md) | [简体中文](./zh.md)

## Build

Recommended clone the **newest** origin repositoies instead of this reposiroty.

```bash

### Not recommended clone this repository with the submodules
git clone https://github.com/zhangwb1996/widget_previewer.git --recursive

### Recommended 
mkdir widget_perviewer
cd widget_perviewer
git clone https://github.com/zhangwb1996/flutter_demo_previewer.git -pre
git clone https://github.com/zhangwb1996/widget_design.git -pre
# open with your vscode or other IDE
code . 
# get the packages from pub.dev, something like this:
flutter pub get
# then
cd flutter_demo_previewer

### create a support for your platform (linux, windows, macOS)
flutter create -platform=windows .

### run main of flutter_demo_previewer in your IDE or command

```

## How to new page demo

* Add the single file of your page demo wherever under the path which is `widget_design/lib/src/preview`.
* **Put you target class at the first**.
* A sample example this:

    ```dart
    // put yout target class at the first of all class in your single file
    class TargetClass extends StatefulWidget {
        ...
    }
    class ClassA {
        ...
    }
    class ClassB  {
        ...
    }
    class ClassC {
        ...
    }
    ```

* **Add export into `widget_design/lib/src/preview/widget.dart`**

    ```dart
    export 'file.dart' show TargetClass
    ```

* Run below command at you terminal

    ```shell
    dart cd flutter_demo_previewer

    # generate _builder.dart files
    dart ./lib/tools/dir/dynamic_widget_helper.dart pre

    # clean and regenerate all the _builder.dart files
    dart ./lib/tools/dir/dynamic_widget_helper.dart clean
    dart ./lib/tools/dir/dynamic_widget_helper.dart pre
    ```

* **hot-reload is not supported, so restart this App**. Then you can search it by name of your target class, and preview it in this App.

## Release

> **Extract Release to the same directory as `widget_design`**

![WDP](https://github.com/zhangwb1996/screenshot/blob/main/WDP/WDP.v1.0.0.gif)

## Awesome Packages

| Pub | Repository |
| ----|---- |
| [json_dynamic_widget](https://pub.dev/packages/json_dynamic_widget)         | [json_dynamic_widget](https://github.com/peiffer-innovations/json_dynamic_widget)
| [provider](https://pub.dev/packages/provider)                               | [provider](https://github.com/rrousselGit/provider)
| [flutter_treeview](https://pub.dev/packages/flutter_treeview)               | [flutter_treeview](https://bitbucket.org/kevinandre/flutter_treeview/src/master/)
| [flutter-code-editor](https://pub.dev/packages/flutter_code_editor/install) | [flutter-code-editor](https://github.com/akvelon/flutter-code-editor)
| [highlight](https://pub.dev/packages/highlight)                             | [highlight](https://github.com/git-touch/highlight.dart)
| [Blur](https://pub.dev/packages/blur)                                       | [Blur](https://github.com/jagritjkh/blur)
