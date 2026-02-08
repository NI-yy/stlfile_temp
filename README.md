# オブジェクトの効率的な回転操作を可能とするトラックボール型VRコントローラ

本リポジトリは，論文「オブジェクトの効率的な回転操作を可能とするトラックボール型VRコントローラ」のプロトタイプ実装において使用した3Dプリント用STLファイルを公開するものです．

## 概要の動画(WISS2025投稿時点)

https://github.com/user-attachments/assets/62c76dcf-048d-4372-a7d2-90046dcec173


## 注意

この実装はハードウェアに損傷を与える可能性があります．使用にあたっては自己責任でお願いします．これらの条件に同意いただけない場合はこのファイルを使用しないでください．

## 内容物 (Contents)

本リポジトリに含まれるSTLファイルは以下の通りです．各パーツは，既存の公開モデルを元に，本プロトタイプ用に調整・統合を行ったものです．

- **トラックボール保持部 (Ball Holder)**
    - `ballHolder_34mm.stl`: 34mmトラックボール用
    - `ballHolder_40mm.stl`: 40mmトラックボール用
    - *元モデル*: [ParRotHardware](https://github.com/ParRot-3DMouse/ParRotHardware)
        - コントローラを傾けた際に球が落下しないように調整を行いました
        - `25mm_upside_for_3360_join.stl`の一部にも使用されています

- **コントローラ上部カバー・アタッチメント (Upside / Attachment)**
    - `25mm_upside_for_3360_join.stl`: 25mm球用の保持部と上部カバーが統合されたパーツ
    - `34mm_body_upside.stl`: 34mm球用の上部カバー
    - `40mm_body_upside.stl`: 40mm球用の上部カバー
    - `upper_attachment.stl`: 上部固定用のパーツ
    - *元モデル*:
        - [HTC Vive Joystick mod.](https://www.thingiverse.com/thing:2705398) (Thingiverse)
        - [SteamVR Unity Plugin - v2.8.0 (sdk 2.0.10)](https://github.com/ValveSoftware/steamvr_unity_plugin/tree/master) (Valve)

- **コントローラ下部カバー (Downside)**
    - `body_downside.stl`: コントローラ下部固定パーツ
    - *元モデル*: [SteamVR Unity Plugin - v2.8.0 (sdk 2.0.10)](https://github.com/ValveSoftware/steamvr_unity_plugin/tree/master) (Valve)

## 組み立て (Assembly)

1. **出力**: 提供されているSTLファイルを3Dプリンタで出力してください．本研究ではPETGフィラメントを使用しました．
2. **必要部品**:
    - HTC VIVE コントローラ
    - PMW3360 イメージセンサ x2
    - Arduino Nano Every
    - トラックボール (直径25mm, 34mm, または 40mm)
3. **配線**: 論文内の記述に従い，PMW3360センサーとArduino Nano Everyを接続してください．
4. **組み立て**: 出力したパーツをVIVEコントローラに装着します．
    - 34mmと40mmのトラックボール保持部とコントローラ上部カバーは接着剤等で接着してください
        - 操作時の親指の疲労を防ぐため，組み立て時になるべくトラックボール保持部の位置が低くなるように接着してください
        - 25mmのトラックボール保持部は体積が小さいため，再現性を優先してstlファイルを統合しました

## 出版物 (Publication)

岩井 望, 阿部 優樹, 坂本 大介

本プロジェクト・成果物を研究等で利用される場合は，論文が出版され次第，引用をお願いいたします．

## ライセンスと謝辞 (License & Acknowledgements)

本リポジトリの3Dモデルは，研究の再現性を担保するために公開されています．各モデルは以下の著作物およびオープンソースハードウェアを元に作成（改変）されました．

1.  **ParRot** ([GitHub](https://github.com/ParRot-3DMouse/ParRotHardware)): ボール保持部分の設計に利用しました．このモデルは**GNU Lesser General Public License v2.1**ライセンスです．
2.  **HTC Vive Joystick mod. by 3DaptiveClint** ([Thingiverse](https://www.thingiverse.com/thing:2705398)): アタッチメント機構（特に上部）の設計に利用しました．このモデルは **CC-BY-NC 4.0** (表示 - 非営利 4.0 国際) ライセンスです．
3.  **SteamVR Unity Plugin - v2.8.0** (Valve): コントローラのカバー部分の設計に利用しました．本リポジトリにはValve社が著作権を有するモデルデータ自体は含まれていません

## 連絡先 (Contact)

岩井 望 / Nozomu Iwai
(連絡先情報があればここに記載)
