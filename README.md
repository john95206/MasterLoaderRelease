## Introduction

![createAllMasterInstaller](https://user-images.githubusercontent.com/22868752/172049874-7026989c-b6f9-40cd-bd61-4cdfeac6a81c.gif)

MasterLoader は Googleスプレッドシート で管理するデータをUnityで読み込み、扱いやすいデータに格納する Unityアセットです。

特に、以下のようなデータの管理に非常に有効です。
- キャラクターデータ（ID、名前、ステータスなど）
- アイテムデータ（ID、名前、効果など）
- 翻訳データ（ID、もとのテキスト、日本語訳、英語訳、など）

編集・作成したスプレッドシートのマスターデータは、MasterLoader によって UnityEditor 上でいつでも取得できます。
取得されたマスターデータは ScriptableObject として Editor上/ゲーム中に限らずいつでも参照できる形で自動的に格納されます。[（ScriptableObjectとは？）](https://docs.unity3d.com/ja/2018.4/Manual/class-ScriptableObject.html)

同時に、作成された ScriptableObject を参照できる Prefab (MasterInstaller) も作成されます。

## Features

### Loader

スプレッドシートのデータを読み込むと同時に、ScriptableObject に値を格納、MasterInstaller に格納したデータを参照させます

![createMaster](https://user-images.githubusercontent.com/22868752/172363988-1a35c195-eed1-4150-8181-d5d752698814.gif)

![UpdateData](https://user-images.githubusercontent.com/22868752/172365155-e2ed8859-b4cd-4850-ae23-8f0507dc59e0.gif)

### MasterInstaller

Loader で格納したデータを参照するPrefab。
Loader でスプレッドシートのデータを読み込むときに自動生成・自動更新されます。
更新は Prefab の MasterInstaller コンポーネントにのみ行われるため、この Prefab に好きなコンポーネントを追加したりカスタマイズできます。
ただし、MasterInstaller の Prefab には MasterInstaller コンポーネントが自動で Add されるため、このコンポーネントを削除するのは推奨されません。

### SheetCreator

MasterLoader で読み込み可能な形で Googleスプレッドシートを任意の Googleドライブフォルダに作成します。

![SheetCreator](https://user-images.githubusercontent.com/22868752/172365711-ec504d8d-c683-4638-8fca-715b1c81443a.gif)

MasterLoader は読み込み可能な形であれば、どんなスプレッドシートでもよいので、この手順はスキップすることができます。
ただし、MasterLoader が読み込むためには以下の要件を満たすシートである必要があります。

- 一行目に各変数の定義が入力してあること
- 二行目に各変数の型が入力してあること
- 三行目に各変数のコメントが入力してあること（特にコメントがなければ空白でよいですが、その場合は三行目を残しておく必要があります）

## Help

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/john95206/MasterLoaderRelease/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
