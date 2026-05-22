# AI

Personal ML repo: self-study, university coursework, portfolio projects.

## Structure

```
AI/
├── study/          # notebooks & exercises (numpy, EDA, ML basics, DL intro)
├── university/     # homework, midterm, retake, y1_y2 assignments
├── projects/       # portfolio (CNN, YOLO)
├── archive/        # finished / one-off work (team project, OULAD, case studies)
├── data/raw/       # shared CSVs for study notebooks (not in git if large)
└── shared/         # reusable code (add when used by 2+ projects)
```

## Projects

| Folder | Description |
|--------|-------------|
| `projects/cast_defect_cnn` | Cast defect classification (CNN + Streamlit) |
| `projects/chair_detection_yolo` | Chair detection (YOLOv8) |

See each project's `README.md` for train/infer commands.

## Data

- **Study notebooks** → `../../data/raw/<file>.csv`
- **Project data** → inside `projects/<name>/data/`
- **University** → CSV next to notebook (do not move before submission)

Large CSVs and YOLO `dataset.zip` use **Git LFS**. CNN project: [separate repo](https://github.com/mentisVeritas/cnn-cast-defect-classification).

```bash
git lfs install && git lfs pull
unzip -q -o projects/chair_detection_yolo/data/dataset.zip -d projects/chair_detection_yolo/data
```

## PyCharm

- Open `Learning/` as workspace; git root is `AI/`.
- Use a separate interpreter per project under `projects/`.
