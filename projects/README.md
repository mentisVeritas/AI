# Projects

## On GitHub (this page)

| Folder | Type |
|--------|------|
| `cnn-cast-defect-classification @ …` | **Git submodule** → [own repo](https://github.com/mentisVeritas/cnn-cast-defect-classification) |
| `chair_detection_yolo/` | tracked in **AI** repo |

The `@ commit` link on GitHub means: parent repo pins a specific version of the nested project repo.

## Clone

```bash
# Parent only
git clone git@github.com:mentisVeritas/AI.git

# Parent + all submodules (CNN code + LFS data)
git clone --recurse-submodules git@github.com:mentisVeritas/AI.git

# Or after clone
git submodule update --init --recursive
cd projects/cnn-cast-defect-classification
git lfs pull && bash scripts/unpack_dataset.sh
```

## Local workspace (PyCharm)

- `cnn-cast-defect-classification/` stays at `projects/cnn-cast-defect-classification/`
- own `.git`, own `git push` inside that folder
- parent `AI` only stores the **commit pointer** (submodule), not project files

## YOLO (in this repo)

```bash
cd chair_detection_yolo
unzip -q -o data/dataset.zip -d data
```
