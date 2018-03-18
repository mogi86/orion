# orion

## Overview

負荷試験ツール「Gatling」の使い方をまとめたリポジトリ。

## Requirement
- Homebrew
- sbt
- scala

## Usage

- Gatlingのダウンロード
    - [こちら](https://gatling.io/download/)よりダウンロード
    - `~/work`配下にバージョン2.3.1のgatlingをダウンロードしたと仮定。

```
~/work/gatling-charts-highcharts-bundle-2.3.1
```

- sbtインストール

```
$ brew install sbt
```

- scalaインストール

```
$ brew install scala
```

- テスト実行

```
$ cd ~/work/gatling-charts-highcharts-bundle-2.3.1
$ sh bin/gatling.sh

Choose a simulation number:
     [0] computerdatabase.BasicSimulation
     [1] computerdatabase.advanced.AdvancedSimulationStep01
     [2] computerdatabase.advanced.AdvancedSimulationStep02
     [3] computerdatabase.advanced.AdvancedSimulationStep03
     [4] computerdatabase.advanced.AdvancedSimulationStep04
     [5] computerdatabase.advanced.AdvancedSimulationStep05

テスト対象の番号を入力し、Enter
その後2回ほど入力を求められるが、特に何も入力せずにEnter
```

- テスト結果をブラウザで確認
    - `/*******/`は対象のディレクトリ。テスト実行時にパスが出力されるのでそれを入力する。

```
$ cd ~/work/gatling-charts-highcharts-bundle-2.3.1
$ open results/*******/index.html
```

- 自分でソースコードを用意する
    - `user-files/simulations/computerdatabase/advanced/`配下にscalaファイルを作成する。
