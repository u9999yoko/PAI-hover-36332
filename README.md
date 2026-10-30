# Physical AI Drone Hovering Experiment

## 概要
Genesis公式のドローン強化学習サンプルを使用し、PPOによる学習と、異なる学習チェックポイントでの目標追従性能を比較した。

## 元コード
[Genesis World — Drone Examples](https://github.com/Genesis-Embodied-AI/genesis-world/tree/main/examples/drone)

本実験はGenesis公式サンプルをベースとしている。強化学習アルゴリズムおよび基本的なドローン制御は独自実装ではない。

## 変更点
- 評価時のドローンと目標座標の距離を記録
- 目標到達判定をCSVに出力
- チェックポイント100・200・300の比較
- 提出動画の長さを調整するため、評価ステップ数を変更

## 結果
300反復時点では目標到達回数が最多となった。一方、200反復時点では平均目標距離が最小となった。

このため、200反復前後が学習量と目標追従性能の妥協点となる可能性がある。ただし、評価時の乱数条件が統一されていないため、最適な学習回数を確定したものではない。

## 使用技術
- Genesis
- PPO（rsl-rl）
- Python / PyTorch

## 出典・ライセンス

本課題では、[Genesis公式リポジトリのDrone Examples](https://github.com/Genesis-Embodied-AI/genesis-world/tree/main/examples/drone) を基に、ドローンの強化学習と評価を実施した。

公式コードの学習アルゴリズムおよび基本的な制御処理を利用し、評価時の目標距離・到達判定のCSV記録機能を追加した。また、学習チェックポイント100・200・300の比較を行った。

元コード：Genesis Authors / Genesis-Embodied-AI

ライセンス：Apache License 2.0

[Genesis公式LICENSE](https://github.com/Genesis-Embodied-AI/genesis-world/blob/main/LICENSE)

## 参考文献

Genesis Authors (2024). *Genesis: A Generative and Universal Physics Engine for Robotics and Beyond*.

https://github.com/Genesis-Embodied-AI/genesis-world

Acknowledgements（謝辞）

本プロジェクトは、Physical AI応用編の最終課題として実施したものです。

本実験の実施にあたり、Genesis開発チームが公開する Drone Examples を利用しました。公開コードを基に、強化学習の実行、評価処理の拡張および学習チェックポイント間の性能比較を行っています。

ロボットシミュレーション環境と実装例をオープンソースとして公開されているGenesis開発チームおよび貢献者の皆様に感謝いたします。

本リポジトリに含まれる改変コードは、原著者による公式実装ではありません。
