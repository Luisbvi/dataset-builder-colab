# Dataset Builder · Colab notebooks

Training notebooks the Dataset Builder app opens in Google Colab from its Train button.

- [train-polygon.ipynb](https://colab.research.google.com/github/Luisbvi/dataset-builder-colab/blob/main/train-polygon.ipynb): YOLOv8n-seg, for a zip saved as Polygon.
- [train-box.ipynb](https://colab.research.google.com/github/Luisbvi/dataset-builder-colab/blob/main/train-box.ipynb): YOLOv8n, for a zip saved as Box.

In Colab: Runtime → Change runtime type → GPU, paste the Google Drive link of the dataset zip (shared as Anyone with the link) in the Dataset zip cell, then Runtime → Run all. Downloading from Drive is far faster than an upload; left empty, the cell asks for the zip to be uploaded instead.

They are written by desktop-core/src/notebook.rs in Dataset Builder (tests/fixtures/notebook-published-*.ipynb); publish them again from there when it changes.
