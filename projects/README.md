# Projects

## Architecture

| Path | Git | Remote |
|------|-----|--------|
| `cnn-cast-defect-classification/` | **Separate repo** (`.git` inside folder) | `git@github.com:mentisVeritas/cnn-cast-defect-classification.git` |
| `chair_detection_yolo/` | Part of parent **AI** repo | same as `AI/` |

`cnn-cast-defect-classification` is an **independent nested repository**:

- lives inside the workspace at `AI/projects/cnn-cast-defect-classification/`
- has its own history, branches, and `git push`
- is **ignored** by the parent AI repo (see root `.gitignore`)
- this is **not** a git submodule and **not** a monorepo — just a local workspace layout

```text
AI/                          ← parent repo (learning + YOLO)
└── projects/
    ├── cnn-cast-defect-classification/   ← child repo (.git here)
    └── chair_detection_yolo/             ← normal folder in parent
```

## Commands

**CNN project** (run inside nested repo):

```bash
cd projects/cnn-cast-defect-classification
git status
git lfs pull
bash scripts/unpack_dataset.sh
```

**YOLO project** (parent repo):

```bash
cd projects/chair_detection_yolo
unzip -q -o data/dataset.zip -d data
```

## PyCharm / VS Code

- Open `Learning/` or `AI/` as workspace — both repos visible.
- For CNN: mark `projects/cnn-cast-defect-classification` as a separate Git root (PyCharm detects nested `.git` automatically).
- Use a **separate Python interpreter** per project.
