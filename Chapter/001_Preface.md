# POLKADOT: VISION FOR A HETEROGENEOUS MULTI-CHAIN FRAMEWORK DRAFT 1

DR. GAVIN WOOD
FOUNDER, ETHEREUM & PARITY
GAVIN@PARITY.IO

翻訳者：
- Sota Watanabe（Twitter @WatanabeSota）
- Masaki Minamide (Twitter @raika_5179)

## 概要
現在のブロックチェーンアーキテクチャーは拡張性やスケーラビリティに留まらず、様々な問題点を抱えている。私達はこの理由を、簡潔さと正当性という2つのコンセンサスアーキテクチャーの重要な2つの要素が密接に絡むことに起因すると考えている。このペーパーでは、この2つの要素を合わせた混合のマルチチェーンのアーキテクチャを紹介する。これらを2つに区分するとし、最低限のセキュリティと移送性の制限化でも全ての機能性を保つことによって実現した、状態に応じたコアの拡張性の実用的な用途を解説する。スケーラビリティはこれらの2つの機能に対して、分割し統治せよのアプローチで対処されている。信頼されていないパブリックのノードのインセンティブ設計を通してスケーリングアウトするように設計されている。このアーキテクチャの混合性はトラストレスかつ、完全に分散化した“federation”の中で相互運用性を持ち、オープンないしクローズのネットワークがお互いにトラストフリーのアクセスを行うことができ、様々なタイプのコンセンサスシステムに対応することができる。私達は1つ以上のEthereumのような既存のネットワークとバックワードで適合性をもつ方法を実装する。そのようなシステムは世界で商用レベルのスケーラビリティとプライバシーの達成を実装できるシステムとしてベースレベルの要素として提供されると考えている。

## 1.序章
このペーパーは現実的にさらなるブロックチェーンのパラダイムを作っていく過程で取りうる1つの方向性を示唆した技術的な"ビジョン"のサマリーである。また、ブロックチェーン技術の様々な観点での具体的な改善策を提供する開発システムを現時点で可能な限り詳細を述べる。

このペーパーは、公式な詳細仕様書であることを意図していない。また、包括的な最終デザインであるわけでもない。APIやバインディング、言語や使用方法をカバーすることもしない。パラメーターは特定されているが変更が見込まれる極めて実験的なペーパーである。コミュニティーのアイデアや批評によってメカニズムが追加されるかもしれないし、修正、削除されるかもしれない。実験的なエビデンスとプロトタイピングによって何ができて何ができないのかがわかるので、このペーパーの大部分が修正されることもありうる。このドキュメントには様々な部分をより良くするかもしれないアイデアを含むプロトコルの詳細が述べられている。その詳細は初期Proof-of-Concept（実証実験）のベースになるものとして期待されている。最終的に完成する“version 1.0”は本プロジェクトの目的を達成するためのさらなるアイデアが反映され、修正されたプロトコルが基になるだろう。

### 1.1 歴史
- 09/10/2016: 0.1.0-proof1
- 20/10/2016: 0.1.0-proof2
- 01/11/2016: 0.1.0-proof3
- 10/11/2016: 0.1.0