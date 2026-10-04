# AI Studio Repository Structure

このリポジトリは、Work / Codex を利用した Blender・Unity・VRChat 制作のための共通ルール、案件仕様、制作データ、成果物を管理します。

基本的に以下の単位で情報を管理します。

- `standards/` — 全AI・全プロジェクト共通ルール
- `roles/` — Work / Codex の各専門AI向けルール
- `projects/` — A・Bなど個別案件の仕様・進捗・制作データ
- `tools/` — 複数案件から利用する共通ツール
- `releases/` — 完成した成果物
- `templates/` — 新規案件作成用テンプレート

## Directory Structure

```text
ai-studio/
│
├── README.md
├── STUDIO_RULES.md
│
├── standards/
│   ├── VRC_GENERAL.md
│   ├── FILE_NAMING.md
│   ├── DIRECTORY_STRUCTURE.md
│   ├── HANDOFF_RULES.md
│   ├── QUALITY_RULES.md
│   └── HUMAN_GATE_RULES.md
│
├── roles/
│   │
│   ├── work/
│   │   ├── avatar-design-director/
│   │   │   ├── ROLE.md
│   │   │   ├── DESIGN_RULES.md
│   │   │   └── WORKFLOW.md
│   │   │
│   │   ├── world-design-director/
│   │   │   ├── ROLE.md
│   │   │   ├── WORLD_DESIGN_RULES.md
│   │   │   └── WORKFLOW.md
│   │   │
│   │   ├── gimmick-design-director/
│   │   │   ├── ROLE.md
│   │   │   ├── GIMMICK_DESIGN_RULES.md
│   │   │   └── WORKFLOW.md
│   │   │
│   │   └── 3d-art-director/
│   │       ├── ROLE.md
│   │       ├── REVIEW_RULES.md
│   │       └── WORKFLOW.md
│   │
│   └── codex/
│       ├── blender-artist/
│       │   ├── AGENTS.md
│       │   ├── MODELING_RULES.md
│       │   ├── TOPOLOGY_RULES.md
│       │   ├── MATERIAL_RULES.md
│       │   ├── VRC_OPTIMIZATION.md
│       │   └── EXPORT_RULES.md
│       │
│       ├── blender-tools-engineer/
│       │   ├── AGENTS.md
│       │   ├── PYTHON_RULES.md
│       │   ├── BLENDER_API_RULES.md
│       │   ├── ADDON_RULES.md
│       │   ├── GEOMETRY_NODES_RULES.md
│       │   └── TEST_RULES.md
│       │
│       ├── unity-world-engineer/
│       │   ├── AGENTS.md
│       │   ├── UNITY_RULES.md
│       │   ├── VRC_WORLD_RULES.md
│       │   ├── UDONSHARP_RULES.md
│       │   ├── LIGHTING_RULES.md
│       │   └── PERFORMANCE_RULES.md
│       │
│       ├── unity-avatar-engineer/
│       │   ├── AGENTS.md
│       │   ├── VRC_AVATAR_RULES.md
│       │   ├── MODULAR_AVATAR_RULES.md
│       │   ├── ANIMATOR_RULES.md
│       │   ├── PARAMETER_RULES.md
│       │   └── PHYSBONE_RULES.md
│       │
│       └── unity-tools-shader-engineer/
│           ├── AGENTS.md
│           ├── UNITY_EDITOR_RULES.md
│           ├── SHADER_RULES.md
│           ├── HLSL_RULES.md
│           └── TEST_RULES.md
│
├── projects/
│   │
│   ├── sanatorium/
│   │   ├── PROJECT.md
│   │   ├── STATUS.md
│   │   ├── DECISIONS.md
│   │   │
│   │   ├── specs/
│   │   │   ├── WORLD_SPEC.md
│   │   │   ├── ART_DIRECTION.md
│   │   │   └── GIMMICK_SPEC.md
│   │   │
│   │   ├── references/
│   │   │   ├── architecture/
│   │   │   ├── props/
│   │   │   └── materials/
│   │   │
│   │   ├── blender/
│   │   │   ├── scenes/
│   │   │   ├── scripts/
│   │   │   └── assets/
│   │   │
│   │   ├── unity/
│   │   │   ├── Assets/
│   │   │   ├── Packages/
│   │   │   └── ProjectSettings/
│   │   │
│   │   └── reviews/
│   │       ├── renders/
│   │       └── REVIEW.md
│   │
│   └── avatar-a/
│       ├── PROJECT.md
│       ├── STATUS.md
│       ├── DECISIONS.md
│       ├── specs/
│       ├── references/
│       ├── blender/
│       ├── unity/
│       └── reviews/
│
├── tools/
│   ├── blender/
│   │   ├── addons/
│   │   ├── geometry-nodes/
│   │   └── scripts/
│   │
│   └── unity/
│       ├── editor/
│       ├── shaders/
│       └── packages/
│
├── templates/
│   ├── PROJECT_TEMPLATE.md
│   ├── STATUS_TEMPLATE.md
│   ├── DECISIONS_TEMPLATE.md
│   ├── WORLD_SPEC_TEMPLATE.md
│   ├── AVATAR_SPEC_TEMPLATE.md
│   ├── GIMMICK_SPEC_TEMPLATE.md
│   └── REVIEW_TEMPLATE.md
│
└── xxxx/
```

## Responsibility

### `STUDIO_RULES.md`

全AIが最初に確認する最上位ルールです。

個別のBlender・Unityルールはここに書かず、制作全体に関わる原則を定義します。

例：

- 作業開始時に対象案件の `PROJECT.md` と `STATUS.md` を確認する
- 案件固有の決定事項は `DECISIONS.md` に記録する
- 仕様変更時は対応する `SPEC` を更新する
- AI間の引き継ぎはチャット履歴ではなくファイルを基準とする
- Human Gate以外では可能な限り自律的に判断する
- 作業終了時に `STATUS.md` を更新する

---

## `standards/`

役割に依存しない共通規約を管理します。

```text
STUDIO_RULES
      │
      ├── VRC_GENERAL
      ├── FILE_NAMING
      ├── DIRECTORY_STRUCTURE
      ├── HANDOFF_RULES
      ├── QUALITY_RULES
      └── HUMAN_GATE_RULES
```

`HUMAN_GATE_RULES.md` では、AIが自律判断してよい範囲と、人間の承認が必要な範囲を定義します。

---

## `roles/`

AIの「職種」を定義します。

```text
roles/

Work
├── Avatar Design Director
├── World Design Director
├── Gimmick Design Director
└── 3D Art Director

Codex
├── Blender Artist
├── Blender Tools Engineer
├── Unity World Engineer
├── Unity Avatar Engineer
└── Unity Tools & Shader Engineer
```

Work側は主に、

```text
要求
 ↓
設計
 ↓
SPEC
 ↓
レビュー
```

を担当します。

Codex側は、

```text
SPEC
 ↓
実装
 ↓
テスト
 ↓
成果物
```

を担当します。

---

## `projects/`

現在進行中の案件を管理します。

案件ごとに最低限、

```text
PROJECT.md
STATUS.md
DECISIONS.md
```

を持たせます。

### PROJECT.md

「何を作っているのか」を定義します。

### STATUS.md

現在の作業状態を管理します。

```text
Current Phase:
Blender Modeling

Completed:
- World blockout
- Room modeling

In Progress:
- Window modeling

Next:
- Props
- Materials
```

### DECISIONS.md

制作途中で決定した内容を記録します。

チャット履歴ではなく、このファイルを決定事項の正とします。

---

## `specs/`

WorkからCodexへの主要な引き継ぎポイントです。

```text
Work
 │
 ├── WORLD_SPEC.md
 ├── ART_DIRECTION.md
 └── GIMMICK_SPEC.md
          │
          ▼
        Codex
```

Codexはチャット履歴ではなく、原則として `specs/` の内容を実装仕様として扱います。

---

## `reviews/`

AIによるレビュー結果を管理します。

```text
Blender Artist
      │
      ▼
   renders/
      │
      ▼
3D Art Director
      │
      ▼
   REVIEW.md
      │
      ▼
Blender Artist
```

これにより、

```text
制作
 ↓
レンダリング
 ↓
レビュー
 ↓
修正
 ↓
再レンダリング
```

のループを人間の介入を減らしながら実行できます。

---

## `tools/`

案件に依存しない再利用可能なツールを管理します。

Blender：

```text
addons/
geometry-nodes/
scripts/
```

Unity：

```text
editor/
shaders/
packages/
```

---

# AI Workflow

基本的な制作フローは以下です。

```text
User
 │
 ▼
Work Director
 │
 │ 企画・設計
 ▼
SPEC
 │
 ▼
Codex Engineer / Artist
 │
 │ Blender / Unity
 ▼
Working Asset
 │
 ▼
Work Reviewer
 │
 ├── NG ──────→ Codex
 │               │
 │               └── 修正
 │
 └── OK
      │
      ▼
     QA
      │
      ▼
  releases/
```

人間は主にHuman Gateとして、

```text
コンセプト承認
重大な仕様変更
最終承認
```

に参加します。

それ以外の制作・レビュー・修正・技術判断については、可能な限りAI側で完結させます。
