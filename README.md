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
| `projects/cnn-cast-defect-classification @ …` | **submodule** | [separate repo](https://github.com/mentisVeritas/cnn-cast-defect-classification) |

On GitHub the `@` hash is the pinned submodule commit (like a dependency version).

```bash
git clone --recurse-submodules git@github.com:mentisVeritas/AI.git
# or: git submodule update --init

cd projects/cnn-cast-defect-classification
git lfs pull && bash scripts/unpack_dataset.sh
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
