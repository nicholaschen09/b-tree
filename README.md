# B-Tree Visualizer

An interactive Jupyter notebook for visualizing B-tree operations step-by-step, including insertions, deletions, splits, and merges.

## Features

- **Step-by-step visualization** of all B-tree operations
- **Interactive controls** using Jupyter widgets
- **Visual highlights** for keys being operated on
- **Detailed step descriptions** explaining each operation
- **Support for insertions** with automatic split visualization
- **Support for deletions** with merge and borrow visualization
- **Configurable minimum degree** (t) for the B-tree

## Installation

1. Install `uv` if you haven't already:
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

2. Install dependencies using `uv`:
```bash
uv sync
```

Or install in development mode:
```bash
uv pip install -e .
```

3. Open the notebook:
```bash
uv run jupyter notebook b_tree_visualizer.ipynb
```

Or activate the virtual environment and run:
```bash
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
jupyter notebook b_tree_visualizer.ipynb
```

## Usage

1. **Run all cells** in the notebook to initialize the visualizer
2. Use the interactive controls to:
   - Set the minimum degree (t) of the B-tree
   - Insert keys by entering a value and clicking "Insert"
   - Delete keys by entering a value and clicking "Delete"
   - Navigate through operation steps using "Previous Step" and "Next Step"
   - Reset the tree to start fresh

## Visual Features

- **Green nodes**: Leaf nodes
- **Gray nodes**: Internal nodes  
- **Red highlight**: Keys being operated on in the current step
- **Step description**: Text description of what's happening at each step

## How It Works

The visualizer tracks every step of B-tree operations:

- **Insertions**: Shows traversal, leaf insertion, and node splits
- **Deletions**: Shows key removal, predecessor/successor replacement, borrowing from siblings, and node merges

Each operation creates a sequence of steps that can be navigated forward and backward to understand the algorithm's behavior.
