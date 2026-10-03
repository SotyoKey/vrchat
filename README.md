## Directory Structure

```text
vrchat/
├── .github/                           # Issue/PRテンプレートなど
├── _guidelines/                       # 【共通仕様・制作規約】各ChatGPTプロジェクトのカスタム指示書用
│   ├── blender/
│   │   ├── modeling_standards.md      # スケール、原点、トポロジー、ポリゴン目標
│   │   └── export_preset.md          # FBXエクスポート設定、軸、UVチャンネル規約
│   ├── unity/
│   │   ├── world_setup_rules.md       # レイヤー、コライダー、Staticフラグ、ベイク設定
│   │   └── avatar_setup_rules.md      # Modular Avatar構成、FXレイヤー規約
│   └── gimmicks/
│       ├── udon_specs.md              # ワールド用Udon / UdonSharp実装標準・同期仕様
│       └── expression_specs.md        # アバター用Expressions Menu・Parameters規約
├── avatars/                           # 【アバター制作案件】
│   └── 001_project_name/
│       ├── 01_design/                 # [VRCアバターデザイン]
│       │   ├── concept.md             # コンセプト、衣装・素体設定
│       │   └── references/            # 三面図、参考画像
│       ├── 02_gimmicks/               # [VRCアバターギミック実装]
│       │   ├── fx_parameters.md       # メニュー構成、パラメータ一覧
│       │   └── animations/            # アニメーション遷移・制御仕様
│       └── assets_status.md           # 進捗、テクスチャ/FBX出力チェックリスト
├── worlds/                            # 【ワールド制作案件】
│   └── 001_project_name/
│       ├── 01_design/                 # [VRCワールド設計]
│       │   ├── concept.md             # 世界観、用途、想定滞在人数
│       │   ├── layout.md              # 空間レイアウト、動線、平面図案
│       │   └── lighting_concept.md    # 昼夜設定、演出意図、色温度
│       ├── 02_modeling/               # [Blenderモデリング]
│       │   ├── rough_blockout.md      # ラフモデルすり合わせ結果
│       │   ├── mesh_specs.md          # 静的/動的メッシュ分離表、ポリゴン割り振り
│       │   └── scripts/               # 自動生成用Blender Pythonスクリプト
│       ├── 03_props/                  # [VRCギミック/小物設計]
│       │   ├── prop_list.md           # 配置小物一覧、Tripo3D投入状況
│       │   └── ortho_views/           # ChatGPT生成の直交三面図
│       ├── 04_unity_setup/            # [VRCワールドセットアップ]
│       │   ├── scene_layout.md        # Prefab配置構成、コライダー定義
│       │   └── bake_settings.md       # Lightmap・Reflection Probe設定
│       ├── 05_gimmicks/               # [VRCワールドギミック実装]
│       │   ├── gimmick_list.md        # スイッチ・トグル一覧、同期仕様
│       │   └── udon_scripts/          # Udon/U# スクリプト設計書・コード
│       └── assets_status.md           # FBX/テクスチャ/ビルド容量チェックリスト
└── releases/                          # 【成果物・配布・バックアップ】
    ├── avatar_gimmicks/               # 配布用アバターギミック (.unitypackage, MAプレハブ等)
    │   └── 001_gimmick_name/
    │       ├── package/               # .unitypackage や Prefab
    │       └── README.md              # 導入手順書・利用規約
    ├── worlds/                        # 公開・納品用ワールド完成パッケージ
    │   └── 001_world_name/
    │       ├── unitypackage/          # シーン・アセット一式
    │       └── build_info.md          # VRChatアップロード情報・推奨設定
    └── world_gimmicks/                # 単体切り出しワールドギミック (UdonSharp, スイッチ等)
        └── 001_switch_system/
            ├── package/               # .unitypackage や プレハブ
            └── README.md              # 組み込み手順・同期仕様説明
```
