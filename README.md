# Labelme (Custom Version)

A customized version of **Labelme** with several additional features to improve the annotation workflow.

---

## Installation

### 1. Create a Conda environment

```bash
conda create -n labelme python=3.11
conda activate labelme
```

### 2. Clone the repository

```bash
git clone <repository_url>
cd labelme
```

### 3. Install Labelme

```bash
pip install -e .
```

---

## Usage

Launch Labelme with a dataset directory:

```bash
labelme <dataset_directory>
```

Example:

```bash
labelme ./dataset
```

---

## Custom Features

This customized version includes the following enhancements:

### Keyboard Shortcuts

| Shortcut | Description |
|----------|-------------|
| **Space** (Edit Mode) | Toggle visibility of the currently selected bounding box. |
| **Ctrl + `** | Exit drawing mode and switch back to **Edit Mode**. |
| **Ctrl + T** | Convert all selected shapes into axis-aligned 4-point rectangles. |

### Additional Features

- **File Progress Indicator**
  - Displays the current file index in the format:
    ```
    4 / 100
    ```
    indicating the current image number and the total number of images.

- **Resume Previous Session**
  - Automatically remembers the last opened file.
  - When Labelme is reopened, it resumes from the last annotated image.

---

## Notes

- The added shortcuts are only available in this customized version.
- Existing Labelme functionality remains unchanged unless otherwise specified.