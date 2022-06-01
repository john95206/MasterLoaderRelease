## Introduction

MasterLoader は Unityアセットです。
MasterLoader によって、 ゲーム内で参照する様々なデータを Google スプレッドシートで管理することができます。

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

### MasterInstaller

Loader で格納したデータを参照するPrefab。

### SheetCreator


For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/john95206/MasterLoaderRelease/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
