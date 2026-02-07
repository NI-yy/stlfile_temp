# 効率的な遠距離オブジェクトの回転操作を可能とするトラックボール型VRコントローラ

本リポジトリは，論文「効率的な遠距離オブジェクトの回転操作を可能とするトラックボール型VRコントローラ」で提案されたプロトタイプの3Dプリント用STLファイルを公開するものです．

## 概要

<img src="./images/prototype_high.png" width="600">
<!-- 画像パスは実際のものに合わせて変更してください -->

本プロジェクトでは，トラックボールを統合することで，遠距離にあるオブジェクトの効率的な3次元回転操作を可能にする新しいVRコントローラを提案しています．標準的なVRコントローラ（HTC VIVEコントローラ）にトラックボールモジュールを後付けすることで，ユーザは精密かつ直感的な回転操作を行うことができます．

## 特徴

- **3DoF回転操作**: 親指でのトラックボール操作により、3自由度（3DoF）の回転入力が可能です。
- **後付け可能な設計**: 既存のHTC VIVEコントローラのトラックパッド部分に装着できる設計です。
- **3Dプリント可能**: カスタムパーツはすべて3Dプリンタで出力可能です。

## 内容物 (Contents)

本リポジトリに含まれるSTLファイルは以下の通りです．各パーツは、既存の公開モデルを元に、本プロトタイプ用に改変・統合・調整を行ったものです。

- **トラックボール保持部 (Ball Holder)**
    - `ballHolder_34mm.stl`: 34mmトラックボール用
    - `ballHolder_40mm.stl`: 40mmトラックボール用
    - *元モデル*: [ParRotHardware](https://github.com/ParRot-3DMouse/ParRotHardware) (西村ら)

- **コントローラ上部・結合部 (Upside / Attachment)**
    - `25mm_upside_for_3360_join.stl`: 25mm球用の保持部と上部カバーが統合されたパーツ
    - `controller_upside_34mm_v2.stl`: 34mm球用の上部カバー
    - `controller_upside_40mm.stl`: 40mm球用の上部カバー
    - `controller_upside_Tsume.stl`: 上部固定用パーツ（爪付き）
    - *元モデル*:
        - [HTC Vive Joystick mod.](https://www.thingiverse.com/thing:2705398) (Thingiverse): スナップフィット機構の参考
        - SteamVR Plugin (Valve): コントローラ形状の適合調整用

- **コントローラ下部 (Downside)**
    - `controller_downside_Tsume.stl`: コントローラ下部固定パーツ
    - *元モデル*: SteamVR Plugin (Valve)

## 組み立て (Assembly)

1. **出力**: 提供されているSTLファイルを3Dプリンタで出力してください．耐久性の観点からPETGフィラメントの使用を推奨します．
2. **必要部品**:
    - HTC VIVE コントローラ
    - PMW3360 モーションセンサー x2
    - Arduino Nano Every
    - トラックボール (直径25mm, 34mm, または 40mm)
    - USBケーブル
3. **配線**: 論文内の記述に従い，PMW3360センサーとArduino Nano Everyを接続してください．
4. **組み立て**: 出力したパーツをVIVEコントローラに装着します．

## 発表文献 (Publication)

**効率的な遠距離オブジェクトの回転操作を可能とするトラックボール型VRコントローラ**
岩井 望, 阿部 優樹, 坂本 大介
*日本ソフトウェア科学会 (JSSST) 第33回インタラクティブシステムとソフトウェアに関するワークショップ (WISS 2025)*

本プロジェクト・成果物を研究等で利用される場合は，論文が出版され次第，引用をお願いいたします．

## ライセンスと謝辞 (License & Acknowledgements)

本リポジトリの3Dモデルは，研究の再現性を担保するために公開されています．各モデルは以下の著作物およびオープンソースハードウェアを元に作成（改変）されました．

1.  **ParRot** ([GitHub](https://github.com/ParRot-3DMouse/ParRotHardware)): ボール保持部分の設計に利用しました．
2.  **HTC Vive Joystick mod. by 3DaptiveClint** ([Thingiverse](https://www.thingiverse.com/thing:2705398)): アタッチメント機構（特に上部）の設計に利用しました．このモデルは **CC-BY-NC 4.0** (表示 - 非営利 4.0 国際) ライセンスです．
3.  **SteamVR Tracking System** (Valve): コントローラとの勘合部分の設計に利用しました．

以上の理由から，本リポジトリに含まれるデータは **CC-BY-NC 4.0** (表示 - 非営利 4.0 国際) ライセンスの下で提供されます．
営利目的での利用はできませんが，研究目的などの非営利利用においては自由に改変・使用いただけます．

## 連絡先 (Contact)

岩井 望 / Nozomu Iwai
(連絡先情報があればここに記載)