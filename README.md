# AI

Main learning / workspace repository: study, university, archive, and in-repo projects.

**GitHub:** [mentisVeritas/AI](https://github.com/mentisVeritas/AI)

## Structure

```
AI/
├── study/              # self-study notebooks (numpy, EDA, ML, DL)
├── university/         # coursework (homework, midterm, retake)
├── projects/           # see projects/README.md
├── archive/            # finished one-off work
├── data/               # shared CSVs for study (large → Git LFS)
└── shared/             # reusable code (when used by 2+ projects)
```

## Projects

| Folder | In this repo? | Notes |
|--------|---------------|--------|
| `projects/chair_detection_yolo/` | yes | YOLOv8, `dataset.zip` via LFS |
| `projects/cnn-cast-defect-classification/` | **no** | nested independent repo — own `.git`, own GitHub |

CNN details: [cnn-cast-defect-classification](https://github.com/mentisVeritas/cnn-cast-defect-classification)

## Nested repository (CNN)

`projects/cnn-cast-defect-classification/` is intentionally **not** part of this repo:

- separate git history and `origin`
- listed in `.gitignore` so parent never tracks its files
- not a submodule — stays on disk inside the workspace for PyCharm

```bash
# Parent AI repo
cd /path/to/AI
git pull
git lfs pull

# Nested CNN repo
cd projects/cnn-cast-defect-classification
git pull
git lfs pull
bash scripts/unpack_dataset.sh
```

## Data (this repo)

| Size | Storage |
|------|---------|
| Large CSVs, `studentVle.csv`, YOLO `dataset.zip` | Git LFS |
| Small CSVs (`Mall_Customers`, `Clean_SuperStore`, …) | regular git |

```bash
git lfs install && git lfs pull
unzip -q -o projects/chair_detection_yolo/data/dataset.zip -d projects/chair_detection_yolo/data
```

## PyCharm

- Workspace root: `Learning/` (all courses) or `AI/` (this repo only).
- Two Git roots: `AI/` + `projects/cnn-cast-defect-classification/`.
- Separate interpreter per project.
