# GameManager - Unity Dynamic Method Invoker

## 概要

- `GameManager`は、指定されたキーを押すことで、任意のMonoBehaviourスクリプト上のメソッドを動的に実行するスクリプトです
- `GameManagerEditor`は、このプロセスを簡単にするために、Unityエディタ内でスクリプトのメソッドを選択するためのカスタムインスペクタを提供します

## 特徴

- MonoBehaviourスクリプト内のメソッドを動的に呼び出し可能
- 引数のないメソッドのみをサポート
- キー入力によってメソッドをトリガー
- カスタムインスペクタでメソッドを簡単に選択可能

## インストール方法

1. git clone

    ``` cmd
    git clone https://github.com/yayoi-exe/unity-method-invoker
    ```

2. Unityプロジェクト内で、`GameManager.cs`および`GameManagerEditor.cs`を適切なフォルダに配置します。

    例えば：
    - `Assets/Scripts/GameManager.cs`
    - `Assets/Editor/GameManagerEditor.cs`
   
## 使い方

1. 任意のゲームオブジェクトに`GameManager`コンポーネントをアタッチします。
2. インスペクタ内で、`Target Script`フィールドに、実行したいスクリプト（MonoBehaviourを継承しているもの）をドラッグ＆ドロップします。
3. `Select Method`のドロップダウンメニューから、実行したいメソッドを選択します。
   - メソッドは引数のないものだけが表示されます。
4. `Activation Key`にはメソッドを実行するためのキーを設定できます。デフォルトはスペースキーです。
5. ゲームをプレイ中に指定したキーを押すと、選択したメソッドが実行されます。

## 注意点

- `Target Script`に指定されたスクリプトは、引数を持たないメソッドのみがサポートされています。
- メソッド名を間違えるとエラーが発生するので、必ず正しいメソッドを選択してください。
