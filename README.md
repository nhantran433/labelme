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

# Custom Features

## Keyboard Shortcuts

### General

| Shortcut | Description |
|----------|-------------|
| **Space** (Edit Mode) | Toggle visibility of the currently selected bounding box. |
| **Ctrl + `** | Exit drawing mode and switch back to **Edit Mode**. |
| **Ctrl + T** | Convert all selected shapes into axis-aligned 4-point rectangles. |

---

### Bounding Box Edge Adjustment

The following shortcuts allow you to move individual edges of the selected bounding box without affecting the opposite edge.

| Shortcut | Action |
|----------|--------|
| **Ctrl + ↑** | Move the **top edge** upward |
| **Ctrl + ↓** | Move the **top edge** downward |
| **Ctrl + ←** | Move the **left edge** left |
| **Ctrl + →** | Move the **left edge** right |
| **Alt + ↑** | Move the **bottom edge** upward |
| **Alt + ↓** | Move the **bottom edge** downward |
| **Alt + ←** | Move the **right edge** left |
| **Alt + →** | Move the **right edge** right |

> **Note:** These shortcuts are fully configurable through the Labelme configuration file.

### Configure Shortcuts

Edit the following file:

```text
~/.labelme/config.yaml
```

Example configuration:

```yaml
shortcuts:
  edge_top_up: Ctrl+Up
  edge_top_down: Ctrl+Down
  edge_left_left: Ctrl+Left
  edge_left_right: Ctrl+Right
  edge_bottom_up: Alt+Up
  edge_bottom_down: Alt+Down
  edge_right_left: Alt+Left
  edge_right_right: Alt+Right
```

You can change any shortcut to your preferred key combination.

---

## Additional Features

### File Progress Indicator

Displays the current image index in the file list.

Example:

```text
4 / 100
```

This indicates that the current image is the 4th image out of 100.

### Resume Previous Session

- Automatically remembers the last opened image.
- Reopens the last annotated image when Labelme is launched again.

---

## Notes

- All added shortcuts and features are available only in this customized version.
- Existing Labelme functionality remains unchanged unless otherwise specified.